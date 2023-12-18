# Timeline

# Data Structure

```sql
CREATE TABLE IF NOT EXISTS `chii_timeline` (
  `tml_id` int unsigned NOT NULL AUTO_INCREMENT,
  `tml_uid` mediumint unsigned NOT NULL DEFAULT '0',
  `tml_cat` smallint unsigned NOT NULL,
  `tml_type` smallint unsigned NOT NULL DEFAULT '0',
  `tml_related` char(255) NOT NULL DEFAULT '0',
  `tml_memo` mediumtext NOT NULL,
  `tml_img` mediumtext NOT NULL,
  `tml_batch` tinyint unsigned NOT NULL,
  `tml_source` tinyint unsigned NOT NULL DEFAULT '0' COMMENT '更新来源',
  `tml_replies` mediumint unsigned NOT NULL COMMENT '回复数',
  `tml_dateline` int unsigned NOT NULL DEFAULT '0',
  PRIMARY KEY (`tml_id`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8;
```

`tml_cat` 一级分类

`tml_type` 二级类型

`tml_related` 直接关联 ID

`tml_memo` 关联数据

`tml_img` 关联图片数据（封面、头像、小组图标等，v2 将废弃）

`tml_batch` 是否为批量数据

# Constants

## Category

```yaml
CAT_DAILY        = 1 #日常行为
CAT_WIKI         = 2 #维基操作
CAT_SBJ_COLLECT  = 3 #收藏
CAT_BGM_PROGRESS = 4 #进度管理
CAT_STATUS       = 5 #吐槽
CAT_BLOG         = 6 #日志
CAT_INDEX        = 7 #目录
CAT_MONO         = 8 #人物
```

## Type

不同 Category 对应二级的 Type

- CAT_DAILY
    
    ```yaml
    注册 = 1
    添加好友 = 2
    加入小组 = 3
    创建小组 = 4
    加入乐园 = 5
    ```
    
- CAT_BGM_PROGRESS
    
    ```yaml
    TYPE_BGM_PROGRESS_BATCH = 0
    TYPE_BGM_PROGRESS_SINGLE = 1
    ```
    
- CAT_STATUS
    
    ```yaml
    TYPE_STATUS_SIGN     = 0
    TYPE_STATUS_TSUKKOMI = 1
    TYPE_STATUS_NICKNAME = 2
    ```
    
- CAT_SBJ_COLLECT 根据条目类型与收藏动作类型进行  Mapping，用于对于不同收藏动作
    
    ```yaml
    #subject_type: { collect_type: tml_type }
    1:  {1:  1, 2:  5, 3:  9,  4:  13, 5:  14}
    2:  {1:  2, 2:  6, 3:  10, 4:  13, 5:  14}
    3:  {1:  3, 2:  7, 3:  11, 4:  13, 5:  14}
    4:  {1:  4, 2:  8, 3:  12, 4:  13, 5:  14}
    6:  {1:  2, 2:  6, 3:  10, 4:  13, 5:  14}
    ```
    
    ```yaml
    1  = 想读
    2  = 想看
    3  = 想听
    4  = 想玩
    5  = 读过
    6  = 看过
    7  = 听过
    8  = 玩过
    9  = 在读
    10 = 在看
    11 = 在听
    12 = 在玩
    13 = 搁置了
    14 = 抛弃了
    ```
    

# V2 tml_memo

php serialize 存储，未来迁移到 json 格式

v2 起，在 `tml_memo` 与中不再存储关联条目详细数据，展示 Timeline 时动态获取条目信息。

- `tml_memo` 中只存储关联条目 id，在展示时通过 `subject_id` 、`ep_id` 等查询对应条目详细信息
- `tml_img` 废弃，不存储图片信息

目前 v2 支持的类型：

- CAT_WIKI
- CAT_SBJ_COLLECT
- CAT_BGM_PROGRESS

### CAT_WIKI 维基编辑

- subject_id

### CAT_SBJ_COLLECT 条目收藏

- `subject_id` 条目 ID
- `collect_id` 收藏 ID
- `collect_comment` 收藏时的吐槽
- `collect_rate` 收藏时的评分

如：

```json
{
  "subject_id": 2,
  "collect_id": 12346,
  "collect_comment": "Amazing",
  "collect_rate": 1
}
```

**同类收藏合并**

如 10 分钟内有同样的收藏类型（，则 `tml_batch` 标记为 1，将 `tml_memo` 合并存储为 {

`{ #subject_id: {}, #subject_id: {} }` 结构。

如：

```json
{
  "2":{
    "subject_id": 2,
    "collect_id": 12346,
    "collect_comment": "Amazing",
    "collect_rate": 1
 },
 "975":{
    "subject_id": 975,
    "collect_id": 12347
 }
}
```

### CAT_BGM_PROGRESS 进度管理

- TYPE_BGM_PROGRESS_BATCH 批量进度
    - `subject_id` 条目 ID
    - `eps_total` 总章节
    - `eps_update` 当前章节
    - `vols_total` 总卷数
    - `vols_update` 当前卷数
- TYPE_BGM_PROGRESS_SINGLE 单条进度
    - `ep_id` 章节 ID
    - `subject_id` 条目 ID
