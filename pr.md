<details>
<summary> 条目 </summary>

GET `/v0/subjects/{subject_id}`

```json
{
  "id": 8,
  "type": 2,
  "name": "コードギアス 反逆のルルーシュR2",
  "name_cn": "Code Geass 反叛的鲁路修R2",
  "summary": "　　“东京决战”一年后，布里塔尼亚少年鲁路修在11区（原日本国）过着平凡的学生生活。但是，鲁路修与弟弟罗洛的一次出行，遇到了黑色骑士团的余党。在与少女C.C再次结成契约之后，尘封的记忆摆在了鲁路修的面前。\r\n　　身为帝国王子的鲁路修，为了建立人人平等的世界、让妹妹娜娜丽幸福的世界，而使用GEASS，令人绝对服从的力量，带领黑色骑士团向帝国宣战。带上假面化名ZERO的他，却在一年前的“东京决战”中被好友朱雀击败，被帝国皇帝抹去了记忆。\r\n　　现在，恢复记忆的鲁路修不仅要面对帝国的强大军事力量，更要面对虚假的弟弟罗洛、失踪的妹妹娜娜丽、不知敌友的中华联盟、内部出现分歧的黑色骑士团。面对内忧外患，鲁路修走上了GEASS之力的诅咒——孤独的王之路。 ",
  "nsfw": false,
  "date": "2008-04-06",
  "platform": 1,
  "images": {
    "large": "https://lain.bgm.tv/pic/cover/l/c9/f0/8_wK0z3.jpg",
    "common": "https://lain.bgm.tv/pic/cover/c/c9/f0/8_wK0z3.jpg",
    "medium": "https://lain.bgm.tv/pic/cover/m/c9/f0/8_wK0z3.jpg",
    "small": "https://lain.bgm.tv/pic/cover/s/c9/f0/8_wK0z3.jpg",
    "grid": "https://lain.bgm.tv/pic/cover/g/c9/f0/8_wK0z3.jpg"
  },
  "infobox": [
    {
      "key": "中文名",
      "value": "Code Geass 反叛的鲁路修R2"
    },
    {
      "key": "别名",
      "value": [
        {
          "v": "叛逆的鲁路修R2"
        },
        {
          "v": "Code Geass: Hangyaku no Lelouch R2"
        },
        {
          "v": "叛逆的勒鲁什R2"
        },
        {
          "v": "叛逆的鲁鲁修R2"
        },
        {
          "v": "コードギアス 反逆のルルーシュR2"
        },
        {
          "v": "Code Geass: Lelouch of the Rebellion R2"
        },
        {
          "v": "叛逆的勒路什R2"
        }
      ]
    },
    {
      "key": "话数",
      "value": "25"
    },
    {
      "key": "放送开始",
      "value": "2008年4月6日"
    },
    {
      "key": "官方网站",
      "value": "http://www.geass.jp/r2/"
    },
    {
      "key": "播放电视台",
      "value": "每日放送"
    },
    {
      "key": "播放结束",
      "value": "2008年9月28日"
    },
    {
      "key": "Copyright",
      "value": "（C）2006 SUNRISE inc./MBS"
    },
    {
      "key": "导演",
      "value": "谷口悟朗"
    },
    {
      "key": "系列构成",
      "value": "大河内一楼"
    },
    {
      "key": "人物原案",
      "value": "CLAMP"
    },
    {
      "key": "人物设定",
      "value": "木村貴宏"
    },
    {
      "key": "美术监督",
      "value": "菱沼由典"
    },
    {
      "key": "色彩设计",
      "value": "岩沢れい子"
    },
    {
      "key": "摄影监督",
      "value": "大矢創太"
    },
    {
      "key": "音响监督",
      "value": "浦上靖夫、井澤基"
    },
    {
      "key": "音乐",
      "value": "中川幸太郎、黒石ひとみ"
    },
    {
      "key": "音乐制作",
      "value": "AUDIO PLANNING U"
    },
    {
      "key": "动画制作",
      "value": "サンライズ"
    }
  ],
  "volumes": 0,
  "eps": 25,
  "total_episodes": 25,
  "rating": {
    "rank": 121,
    "total": 77255,
    "count": {
      "1": 44,
      "2": 15,
      "3": 32,
      "4": 66,
      "5": 145,
      "6": 457,
      "7": 1472,
      "8": 3190,
      "9": 2640,
      "10": 1377
    },
    "score": 8.2
  },
  "collection": {
    "wish": 622,
    "collect": 13216,
    "doing": 147,
    "on_hold": 224,
    "dropped": 115
  }
}
```

</details>

<details>
<summary> 剧集 </summary>

GET `/v0/subjects/{subject_id}/eps`

参数:

- `type` `0,1,2,3` 代表 `本篇，sp，op，ed`
- `limit` 最大 200
- `offset`

章节总数应该从 条目主 api 的`$.total_episodes`获取。

```json
[
  {
    "id": 522,
    "type": 0,
    "sort": 1,
    "name": "魔神 が 目覚める 日",
    "name_cn": "魔王的苏醒之日",
    "duration": "24m",
    "airdate": "2008-04-06",
    "comment": 11,
    "desc": ""
  },
  {
    "id": 523,
    "type": 0,
    "sort": 2,
    "name": "日本独立計画",
    "name_cn": "日本独立计划",
    "duration": "24m",
    "airdate": "2008-04-13",
    "comment": 12,
    "desc": ""
  },
  {
    "id": 524,
    "type": 0,
    "sort": 3,
    "name": "囚われの学園",
    "name_cn": "被囚禁的学园",
    "duration": "24m",
    "airdate": "2008-04-20",
    "comment": 8,
    "desc": ""
  },
  {
    "id": 525,
    "type": 0,
    "sort": 4,
    "name": "逆襲の処刑台",
    "name_cn": "逆行的处刑台",
    "duration": "24m",
    "airdate": "2008-04-27",
    "comment": 20,
    "desc": ""
  },
  {
    "id": 526,
    "type": 0,
    "sort": 5,
    "name": "ナイト オブ ラウンズ",
    "name_cn": "圆桌骑士",
    "duration": "24m",
    "airdate": "2008-05-04",
    "comment": 9,
    "desc": ""
  },
  {
    "id": 527,
    "type": 0,
    "sort": 6,
    "name": "太平洋 奇襲 作戦",
    "name_cn": "太平洋奇袭作战",
    "duration": "24m",
    "airdate": "2008-05-11",
    "comment": 14,
    "desc": ""
  },
  {
    "id": 528,
    "type": 0,
    "sort": 7,
    "name": "棄てられた 仮面",
    "name_cn": "被丢弃的面具",
    "duration": "24m",
    "airdate": "2008-05-18",
    "comment": 18,
    "desc": ""
  },
  {
    "id": 529,
    "type": 0,
    "sort": 8,
    "name": "百万のキセキ",
    "name_cn": "百万的奇迹",
    "duration": "24m",
    "airdate": "2008-05-25",
    "comment": 10,
    "desc": ""
  },
  {
    "id": 530,
    "type": 0,
    "sort": 9,
    "name": "朱禁城の花嫁",
    "name_cn": "朱禁城的花嫁",
    "duration": "24m",
    "airdate": "2008-06-08",
    "comment": 14,
    "desc": ""
  },
  {
    "id": 531,
    "type": 0,
    "sort": 10,
    "name": "神虎輝く刻",
    "name_cn": "神虎闪耀之刻",
    "duration": "24m",
    "airdate": "2008-06-15",
    "comment": 6,
    "desc": ""
  },
  {
    "id": 532,
    "type": 0,
    "sort": 11,
    "name": "想いの力",
    "name_cn": "思念的力量",
    "duration": "24m",
    "airdate": "2008-06-22",
    "comment": 12,
    "desc": ""
  },
  {
    "id": 89,
    "type": 0,
    "sort": 12,
    "name": "ラブ アタック!",
    "name_cn": "爱的初体验",
    "duration": "24m",
    "airdate": "2008-07-01",
    "comment": 15,
    "desc": ""
  },
  {
    "id": 90,
    "type": 0,
    "sort": 13,
    "name": "過去からの刺客",
    "name_cn": "来自过去的刺客",
    "duration": "24m",
    "airdate": "2008-07-06",
    "comment": 21,
    "desc": ""
  },
  {
    "id": 2,
    "type": 0,
    "sort": 14,
    "name": "ギアス 狩り",
    "name_cn": "Geass 狩猎",
    "duration": "24m",
    "airdate": "2008-07-12",
    "comment": 11,
    "desc": ""
  },
  {
    "id": 91,
    "type": 0,
    "sort": 15,
    "name": "C の 世界",
    "name_cn": "C的世界",
    "duration": "24m",
    "airdate": "2008-07-20",
    "comment": 10,
    "desc": ""
  },
  {
    "id": 104,
    "type": 0,
    "sort": 16,
    "name": "超合集国決議第壱號",
    "name_cn": "超合众国决议第一号",
    "duration": "24m",
    "airdate": "2008-07-27",
    "comment": 4,
    "desc": "終に実現した超合集国構想。合衆国日本と合衆国中華を中心に批准した国は47ヵ国。これによりEUは完全に弱体化し世界は超合集国とブリタニアに２分化され、世界は新たな局面を迎える。その最高評議会の場で決議された第壱號とは！"
  },
  {
    "id": 374,
    "type": 0,
    "sort": 17,
    "name": "土の味",
    "name_cn": "土之气味",
    "duration": "24m",
    "airdate": "2008-08-03",
    "comment": 6,
    "desc": ""
  },
  {
    "id": 520,
    "type": 0,
    "sort": 18,
    "name": "第二次 東京 決戦",
    "name_cn": "第二次东京决战",
    "duration": "24m",
    "airdate": "2008-08-10",
    "comment": 12,
    "desc": "キュウシュウで、そしてトウキョウ租界で戦闘が始まった。超合集国の戦力を得た黒の騎士団とナイトオブラウンズをも投入したブリタニア軍。精鋭同士の全面対決は紅蓮聖天八極式の参戦で更に激化していく。そしてその死闘の果ての結末は…"
  },
  {
    "id": 574,
    "type": 0,
    "sort": 19,
    "name": "裏切り",
    "name_cn": "背叛",
    "duration": "24m",
    "airdate": "2008-08-17",
    "comment": 14,
    "desc": "トウキョウ租界の決戦は多くの犠牲者を出してしまった。その混乱を突くかの如く、そのイカルガにブリタニアの特使が訪れた。自ら敵艦に乗り込んできたその人物こそ！？最凶の楔が黒の騎士団に向けられた！？"
  },
  {
    "id": 577,
    "type": 0,
    "sort": 20,
    "name": "皇帝 失格",
    "name_cn": "皇帝 失格",
    "duration": "24m",
    "airdate": "2008-08-24",
    "comment": 7,
    "desc": "ロロによって窮地を脱したルルーシュ。だが、もう彼が辿るべき道は一つしか無い…。同じ頃、ブリタニア軍、黒の騎士団双方で大きなうねりが起きようとしていた。世界は新たな局面を迎えるのか？さらに神根島に降臨したブリタニア皇帝がついに動き出す！！そしてその時、ルルーシュは！？"
  },
  {
    "id": 593,
    "type": 0,
    "sort": 21,
    "name": "ラグナレク の 接続",
    "name_cn": "诸神 黄昏 连接",
    "duration": "24m",
    "airdate": "2008-08-31",
    "comment": 25,
    "desc": "大混乱するエリア11。引き返せない、いや引き返さない。硬く悲壮なまでの決意の元、スザクは戦いに挑む！最強の部隊を相手に彼は勝利する事が出来るのか！？そしてルルーシュもまた…。人智超越した世界で明かされる驚天動地の事実と真実は！？"
  },
  {
    "id": 607,
    "type": 0,
    "sort": 22,
    "name": "皇帝　ルルーシュ",
    "name_cn": "皇帝 鲁路修",
    "duration": "24m",
    "airdate": "2008-09-07",
    "comment": 14,
    "desc": ""
  },
  {
    "id": 609,
    "type": 0,
    "sort": 23,
    "name": "シュナイゼル　の　仮面",
    "name_cn": "修耐泽尔的假面",
    "duration": "24m",
    "airdate": "2008-09-14",
    "comment": 9,
    "desc": ""
  },
  {
    "id": 1343,
    "type": 0,
    "sort": 24,
    "name": "ダモクレスの空",
    "name_cn": "达摩克里斯的天空",
    "duration": "24m",
    "airdate": "2008-09-21",
    "comment": 6,
    "desc": ""
  },
  {
    "id": 1344,
    "type": 0,
    "sort": 25,
    "name": "Re;",
    "name_cn": "Re;",
    "duration": "24m",
    "airdate": "2008-09-28",
    "comment": 21,
    "desc": "最终话"
  }
]
```

</details>

<details>
<summary> 关联人物 </summary>

GET `/v0/subjects/{subject_id}/persons`

响应同 `/v0/persons`

```json
[
  {
    "id": 1,
    "name": "水樹奈々",
    "type": 1,
    "career": ["artist", "seiyu"],
    "images": {
      "large": "https://lain.bgm.tv/pic/crt/l/a6/e8/1_prsn_ZdFfp.jpg?r=1597241889",
      "medium": "https://lain.bgm.tv/pic/crt/m/a6/e8/1_prsn_ZdFfp.jpg?r=1597241889",
      "small": "https://lain.bgm.tv/pic/crt/s/a6/e8/1_prsn_ZdFfp.jpg?r=1597241889",
      "grid": "https://lain.bgm.tv/pic/crt/g/a6/e8/1_prsn_ZdFfp.jpg?r=1597241889"
    },
    "locked": false,
    "short_summary": "原名 近藤 奈々（こんどう なな），日本女性声优兼歌手。有个妹妹名字是近藤美香，为Daisy×Daisy主唱。\r\n\r\n简介\r\n自小受业余经营歌谣教室的父母影响，",
    "img": null
  }
]
```

</details>

<details>
<summary> 出场角色 </summary>

GET `/v0/subjects/{subject_id}/characters`

响应同 `/v0/characters`

```json
[
  {
    "id": 1,
    "name": "ルルーシュ・ランペルージ",
    "type": 1,
    "images": {
      "large": "https://lain.bgm.tv/pic/crt/l/7b/3a/1_crt_8V556.jpg?r=1603459589",
      "medium": "https://lain.bgm.tv/pic/crt/m/7b/3a/1_crt_8V556.jpg?r=1603459589",
      "small": "https://lain.bgm.tv/pic/crt/s/7b/3a/1_crt_8V556.jpg?r=1603459589",
      "grid": "https://lain.bgm.tv/pic/crt/g/7b/3a/1_crt_8V556.jpg?r=1603459589"
    },
    "locked": false,
    "short_summary": "鲁路修·兰佩洛基是日本动画《Code Geass 反叛的鲁路修》中的主角。\r\n\r\n一年前的东京攻略战中，黑色骑士团因为首领Zero的离开而最终战败。之后一年间，"
  },
  {
    "id": 2,
    "name": "枢木スザク",
    "type": 1,
    "images": {
      "large": "https://lain.bgm.tv/pic/crt/l/6f/40/2_crt_08diJ.jpg?r=1581939778",
      "medium": "https://lain.bgm.tv/pic/crt/m/6f/40/2_crt_08diJ.jpg?r=1581939778",
      "small": "https://lain.bgm.tv/pic/crt/s/6f/40/2_crt_08diJ.jpg?r=1581939778",
      "grid": "https://lain.bgm.tv/pic/crt/g/6f/40/2_crt_08diJ.jpg?r=1581939778"
    },
    "locked": false,
    "short_summary": "在第一季的最后，驾驶兰斯洛特向Zero展开了大报复，于战场上活跃，被柯内莉娅晋升为骑士侯。最后在神根岛和鲁路修对决中。从V.V处得知了Geass能力的实质。\r\n"
  },
  {
    "id": 3,
    "name": "C.C.",
    "type": 1,
    "images": {
      "large": "https://lain.bgm.tv/pic/crt/l/83/62/3_crt_7Jhis.jpg?r=1573280268",
      "medium": "https://lain.bgm.tv/pic/crt/m/83/62/3_crt_7Jhis.jpg?r=1573280268",
      "small": "https://lain.bgm.tv/pic/crt/s/83/62/3_crt_7Jhis.jpg?r=1573280268",
      "grid": "https://lain.bgm.tv/pic/crt/g/83/62/3_crt_7Jhis.jpg?r=1573280268"
    },
    "locked": false,
    "short_summary": "在鲁路修面临生死关头时，给予他Geass的力量救了鲁路修一命。目前寄住在鲁路修家中。但是在R2中只出没于黑色骑士团。\r\nC.C.不会容许鲁路修死去，因为她还有“"
  }
]
```

</details>
