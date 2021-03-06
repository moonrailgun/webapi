# 追书神器接口文档

## api服务器地址
`http://api.zhuishushenqi.com`

### 追书架

- **请求URL**
> [/book](http://api.zhuishushenqi.com/book)

- **请求方式**
>**GET**

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
view | string | 查询类型(**updated**)
id | string | 书籍id **可以同时传输多个，用英文,号分割**

- **返回参数**

- **请求示例**
>[/book?view=updated&id=55eef8b27445ad27755670b9](http://api.zhuishushenqi.com/book?view=updated&id=55eef8b27445ad27755670b9)

- **返回示例**

```JSON
[
  {
    "_id": "55eef8b27445ad27755670b9",
    "author": "圣骑士的传说",
    "referenceSource": "default",
    "updated": "2017-06-02T00:35:32.037Z",
    "chaptersCount": 1243,
    "lastChapter": "第1246章 霸宋前辈，要吃糖吗？（求月票）"
  }
]
```

### 模糊搜索

- **请求URL**
> [/book/fuzzy-search](http://api.zhuishushenqi.com/book/fuzzy-search)

- **请求方式**
>**GET**

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
query | string | 搜索名
start | int | 开始位置
limit | int | 条目数限制

- **返回参数**

- **请求示例**
>[/book/fuzzy-search?query=莽荒纪&start=0&limit=100](http://api.zhuishushenqi.com/book/fuzzy-search?query=莽荒纪&start=0&limit=100)

- **返回示例**

```JSON
{
  "books": [
    {
      "_id": "50ce6b1263d90df45a000001",
      "hasCp": true,
      "title": "莽荒纪",
      "cat": "仙侠",
      "author": "我吃西红柿",
      "site": "zhuishuvip",
      "cover": "/agent/http://image.cmfu.com/books/2502372/2502372.jpg",
      "shortIntro": "纪宁死后来到阴曹地府，经判官审前生判来世，投胎到了部族纪氏。 这里， 有夸父逐日…… 有后羿射金乌…… 更有为了逍遥长生，历三灾九劫，纵死无悔的无数修仙者…… ...",
      "lastChapter": "第四十五卷 第十七章 梅花香（大结局下）",
      "retentionRatio": 53.64,
      "banned": 0,
      "latelyFollower": 11308,
      "wordCount": 4180430
    },
    {
      "..."
    }
  ],
  "ok": true
}
```

### 热门搜索

- **请求URL**
> [/book/hot-word](http://api.zhuishushenqi.com/book/hot-word)

- **请求方式**
>**GET**

- **请求参数**

- **返回参数**

- **请求示例**
>[/book/hot-word](http://api.zhuishushenqi.com/book/hot-word)

- **返回示例**

```JSON
{
  "hotWords": [
    "废柴至尊：腹黑大小姐",
    "太易",
    "重生首长的小媳妇",
    "抓鬼小农民",
    "惊世毒妃：轻狂大小姐",
    "九龙神鼎",
    "总裁强势宠：甜妻，有喜了！",
    "升棺发财",
    "特工皇妃楚乔传",
    "帝国重器",
    "冷魅军少：勿惹狂枭帅妻",
    "九天剑主",
    "绝色嚣张九小姐",
    "阴阳鬼咒",
    "重生之国民男神",
    "超级小村民",
    "冷帝宠上天：腹黑狂妃",
    "万龙神尊",
    "天价宠儿：总裁的新妻",
    "大秦帝国之召唤天下",
    "重生归来：天才修炼师",
    "网游之逍遥派大弟子",
    "僵尸萌宝，买一送一",
    "跃马大唐",
    "农门悍女：掌家小厨娘",
    "修真狂少",
    "重生商女：妙手空间猎军少",
    "斩邪",
    "帝宠狂妃：废材千金要逆天",
    "掌珠"
  ],
  "ok": true
}
```


### 书籍信息

- **请求URL**
> [/book/:id](http://api.zhuishushenqi.com/book/:id)

- **请求方式**
>**GET**

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
id | string | 书本id

- **返回参数**

- **请求示例**
>[/book/50ce6b1263d90df45a000001](http://api.zhuishushenqi.com/book/50ce6b1263d90df45a000001)

- **返回示例**

```JSON
{
  "_id": "50ce6b1263d90df45a000001",
  "author": "我吃西红柿",
  "cover": "/agent/http://image.cmfu.com/books/2502372/2502372.jpg",
  "creater": "iPhone 4",
  "longIntro": "纪宁死后来到阴曹地府，经判官审前生判来世，投胎到了部族纪氏。\r\n这里，\r\n有夸父逐日……\r\n有后羿射金乌……\r\n更有为了逍遥长生，历三灾九劫，纵死无悔的无数修仙者……\r\n……\r\n纪宁也成为了一名修仙者，开始了他的修仙之路……\r\n本书已改编为漫画，可下载“漫画岛”APP阅读",
  "title": "莽荒纪",
  "cat": "古典仙侠",
  "majorCate": "仙侠",
  "minorCate": "古典仙侠",
  "currency": 0,
  "contentType": "txt",
  "_le": false,
  "allowMonthly": false,
  "allowVoucher": true,
  "allowBeanVoucher": false,
  "hasCp": true,
  "postCount": 40163,
  "latelyFollower": 11210,
  "followerCount": 73528,
  "wordCount": 4180430,
  "serializeWordCount": 0,
  "retentionRatio": "53.77",
  "updated": "2016-08-03T01:48:15.612Z",
  "isSerial": false,
  "chaptersCount": 1450,
  "lastChapter": "第四十五卷 第十七章 梅花香（大结局下）",
  "gender": [
    "male"
  ],
  "tags": [
    "神魔",
    "热血",
    "洪荒",
    "架空",
    "古典仙侠",
    "修仙",
    "仙侠"
  ],
  "donate": false,
  "copyright": "阅文集团正版授权"
}
```

### 相关推荐

- **请求URL**
> [/book/:id/recommend](http://api.zhuishushenqi.com/book/:id/recommend)

- **请求方式**
>**GET**

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
id | string | 书本id

- **返回参数**

- **请求示例**
>[/book/50ce6b1263d90df45a000001/recommend](http://api.zhuishushenqi.com/book/50ce6b1263d90df45a000001/recommend)

- **返回示例**

```JSON
{
  "books": [
    {
      "_id": "51d12c844a6165603e00002e",
      "title": "灵域",
      "author": "逆苍天",
      "site": "zhuishuvip",
      "cover": "/agent/http://image.cmfu.com/books/2817301/2817301.jpg",
      "shortIntro": "三万年前，自称为“神”的搏天族入侵灵域，百族奋起反抗，最终惨败，人族率先投诚，百族随后相继臣服。 之后万年，所有种族皆被搏天族奴役，被严酷对待，生活在恐怖阴影中...",
      "lastChapter": "第一千八百四十一章 开启新时代！",
      "retentionRatio": 48.78,
      "latelyFollower": 9613,
      "cat": "玄幻",
      "majorCate": "玄幻",
      "minorCate": "东方玄幻"
    },
    {...},
    {...},
  ],
  "ok": true
}
```

### 书籍来源

- **请求URL**
> [/toc](http://api.zhuishushenqi.com/toc)

- **请求方式**
>**GET**

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
view | string | 查询类型(**summary**)
book | string | 书本id

- **返回参数**

- **请求示例**
>[/toc?view=summary&book=50ce6b1263d90df45a000001](http://api.zhuishushenqi.com/toc?view=summary&book=50ce6b1263d90df45a000001)

- **返回示例**

```JSON
[
  {
    "_id": "56f8db7f176d03ac19843c59",
    "source": "zhuishuvip",
    "name": "优质书源",
    "link": "http://vip.zhuishushenqi.com/toc/56f8db7f176d03ac19843c59",
    "lastChapter": "第四十五卷 第十七章 梅花香（大结局下）",
    "isCharge": false,
    "chaptersCount": 1450,
    "updated": "2016-09-14T10:00:08.826Z",
    "starting": true,
    "host": "vip.zhuishushenqi.com"
  },
  {
    "_id": "523815ef08c1c1353b00000b",
    "lastChapter": "莽荒纪TXT全集下载，莽荒纪TXT下载，莽荒纪TXT电子书下载，莽荒",
    "link": "http://leduwo.com/book/29/29930/index.html",
    "name": "乐读窝",
    "source": "tianyibook",
    "isCharge": false,
    "chaptersCount": 1485,
    "updated": "2017-01-14T21:49:48.468Z",
    "starting": false,
    "host": "leduwo.com"
  },
  {
    "_id": "55debbf2007d4d8623de1c6e",
    "lastChapter": "番茄新书《雪鹰领主》五十万字了，可以看了~~",
    "link": "http://api.easou.com/api/bookapp/chapter_list.m?gid=6326585&nid=1006326585&size=10000&cid=eef_easou_book&version=002&os=android&appverion=1011",
    "source": "aeasou",
    "name": "宜搜小说",
    "isCharge": false,
    "chaptersCount": 1492,
    "updated": "2016-11-13T07:15:33.968Z",
    "starting": false,
    "host": "api.easou.com"
  },
  {...}
]
```

### 章节目录

- **请求URL**
> [/toc/:id](http://api.zhuishushenqi.com/toc/:id)

- **请求方式**
>**GET**

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
view | string | 查询类型(**chapters**)
id | string | 书源id

- **返回参数**

- **请求示例**
>[/toc/523815ef08c1c1353b00000b?view=chapters](/toc/523815ef08c1c1353b00000b?view=chapters)

- **返回示例**

```JSON
{
  "_id": "523815ef08c1c1353b00000b",
  "link": "http://leduwo.com/book/29/29930/index.html",
  "name": "乐读窝",
  "chapters": [
    {
      "title": "第一章 地府",
      "link": "http://leduwo.com/book/29/29930/8180151.html",
      "currency": 0,
      "unreadble": false,
      "isVip": false
    },
    {...}
  ],
  "updated": "2017-01-14T21:49:48.468Z",
  "host": "leduwo.com"
}
```

### 章节正文

- **请求URL**
> [http://chapterup.zhuishushenqi.com/chapter/:link]()

- **请求参数**

请求参数 | 参数类型 | 参数说明
------------- | ------------- | -------------
link | string | 章节连接
k | string | 未知 **可选**
t | string | 当前时间戳 **可选**

- **返回参数**

- **请求示例**
>[http://chapterup.zhuishushenqi.com/chapter/http%3A%2F%2Fleduwo.com%2Fbook%2F29%2F29930%2F8180151.html?k=c9aaa4e230c05885&t=1496481986](http://chapterup.zhuishushenqi.com/chapter/http%3A%2F%2Fleduwo.com%2Fbook%2F29%2F29930%2F8180151.html)

- **返回示例**

```JSON
{
  "ok": true,
  "chapter": {
    "title": "第十八章 翼",
    "body": "冲榜关键时刻，番茄需要大家的推荐票！\n————\n“嗯。”纪宁随手一翻，手出现一块泛着青光的金子，直接朝黑蛇男子的摊子上一扔，“给。”\n“就这点金子？”黑蛇汉子和他身后的两汉子都慌了，看着那只有手指头大一点的泛青光的金子，“还不是纯的金子？”\n“公子。”\n“尊敬的公子。”\n这三名汉子都连喊着哀求了，他们怎么和部落交代啊，其他部落战士还在城外等着呢。那些部落战士没舍得进城……因为每人进城都需要缴纳一张角羊皮或者等价物。\n“真是愚蠢，那可是雷金。”\n“我出一百块兽头金，换你这雷金。”\n“才一百块兽头金？这么一块雷金，我愿出一百十兽头金和你换，我现在就安排人将兽头金送来！”顿时旁边那些人都连出价，他们都是西府城颇有些地位的人物，或者是来自先天生灵的家族，或者是一些移居到西府城内的部落的权势人物，眼光何等毒辣？\n黑蛇汉子连一把抓起那块雷金，明显感觉重量远超黄金，和旁边的两名伙伴相视，又惊又喜。\n“谢公子。”\n“谢伟大的公子。”\n三名汉子连激动感谢。\n“现在知道谢了？滴水剑可是声名远播的大人物，他家公子是何等身份，怎么会强抢你们的兵器。人家随便扔出点，就吓蒙你们了。”旁边有一胖胖的兽皮老者高声说着，显然刻意说给旁边不远处的纪宁听。\n纪宁笑了笑，手的一鞘三剑就凭空消失收进了纳晶。因为纳晶空间有限，所以纪宁随身携带的只有几块兽头金，其他则是些贵重宝物等等。\n……\n厅内。\n纪一川依旧高坐在主位，尉迟雪坐在其左手侧边，二人都慢慢吃着面前条案上的食物。\n嗖！\n一道人影冲了进来，正是逛街归来的纪宁。\n“父亲，母亲。”纪宁连道。\n纪一川皱眉：“在外逛街就不看着点时辰？”\n纪宁乖巧着不敢吭声连跑到自己的位置，跪坐下来开始吃起来，午的吃食比较丰富，肉食、面食、酒水等都极多，纪宁现如今的食量那是极大的，整个条案上摆放的大量食物酒水很快就被纪宁完全吃了一空。\n尉迟雪笑看着儿子风卷残云般吃完。\n“父亲，母亲。”纪宁想起今天买的那一鞘三剑，连道，“我今天逛街时碰到三名部落战士，应该是很偏远地带辛苦来到西府城的，他们就是为了卖掉一件神兵。而我……便将这一神兵给买下了。”\n“神兵？”坐在上方的纪一川皱眉，“我纪氏西府宝库内，神兵多的是。之前你不是选过两件神兵吗？城内那些贩卖的兵器哪有什么好货色。”\n因为纪宁未曾达到炼气先天，自然就没办法使用法宝，所以才去府内宝库专门选了两件剑器神兵。当然平常进行困笼之战时，使用的都只是普通兵器。\n“父亲，我在府内宝库选的两件神兵，远不如我选的这件。”纪宁郑重道。\n“哦？”纪一川看向儿子。\n“其实我买的神兵，是一套破损的剑器法宝。”纪宁解释，“上面一些玄妙的纹路完全破碎，所以只能当做锋利点的神兵使用了。不过它的确非常锋利，超过之前我在府内包括所选神兵一大截，甚至我用力，都能用它刺开金辰衣。”\n“刺开金辰衣？”纪一川露出惊色，“给我瞧瞧。”\n纪宁当即一伸手，手出现了那古朴的一鞘三剑，连起身送到了父亲面前。\n纪一川接过后仔细观看，又拔出了三柄剑查看：“剑身上的阵法符完全破碎，不过感应其韵……的确是一套飞剑法宝！可惜是一破损的法宝，一般的破损法宝没多大价值，最多法宝本身熔炼了或许还能提取些许材料出来。”\n纪宁点头。\n他看过很多书籍，也知道破损法宝价值很低，因为破损的法宝本身的材料经过一次炼制混合在一起，即便熔炼提取原始材料，也只能提取少许而已。\n“嗤！”纪一川手指一摸剑锋，指头上一丝血迹渗透而出，令他露出惊色，“好锋利的剑，没有灌输真元元力，剑本身竟然就能这么锋利，我还没见过。雪儿，你来看看，可能看出点来历？”\n尉迟雪接过仔细观察，许久缓缓摇头：“认不出。”\n“母亲，这飞剑法宝在没损坏前，可曾入阶？”纪宁连追问。\n“当然是入阶的法宝。”尉迟雪点头道，“这法宝即便完全破损，它的锋利已经能媲美一些不入阶法宝了。当它完好时……当然是入阶的法宝。只是它是哪一阶的法宝，却是我根本看不出的，恐怕整个燕山大地都没谁能看出。”\n纪宁点头，这点他懂。\n一般炼气先天生灵用的都是不入阶的法宝，紫府修士才能用入阶的法宝。而炼制法宝更艰难……整个燕山大地都没听说谁能亲手炼制法宝，恐怕只有无尽遥远之地一些无比强大的部族，才有能够炼制法宝的强者。\n“大夏王朝是从神魔时代传承至今。”纪一川将一鞘三剑扔给儿子，“它统领的无尽疆域有着亿万年的历史，不知有过多少部族兴盛、衰败、破灭，不知遗留下多少宝藏。一些战斗后破损的法宝更不算罕见，我纪氏这一类破损的法宝，也有数百件之多，大多都说不清来历。这破损的法宝竟能这般锋利，也算难得，正适合你用。”\n尉迟雪更是道：“宁儿，你将来成为炼气先天生灵，真元灌输不入阶的法宝……威力都不一定赶得上它！”\n纪宁点头。\n法宝，强在神秘莫测。\n一般炼气先天神灵使用法宝，自然是千奇百怪。可是神魔炼体流……最擅长的就是近身战，他们拥有着近乎不死的身体，强大的力量、速度、恢复力，所以神魔炼体流即便使用法宝，也是使用刀剑长枪等近身战兵器。\n“这一鞘三剑，即便我成为先天生灵，也依旧适合我用。”纪宁心生喜悦，思索着，“怕在很长时间内都会陪着我，我得给它起个名字……嗯，就叫北冥剑！”\n纪宁突然想到‘北冥’，其实也是有原因的。\n当年父亲纪一川离开燕山这片大地，在无尽大地上不断闯荡，甚至前往北方的无尽大海，那片广袤的大海也被人们称之为‘北冥大海’，在那北冥大海有着很多岛屿，纪一川漂泊着闯荡着，也认识了尉迟雪。\n他们结伴同行，经历生死，最终相爱，尔后怀孕。\n正因为怀孕……他们才会离开危险的北冥大海，要赶回燕山。然而在途几经危险，尉迟雪都受到过重创，这也是为何说‘纪宁在胎里就受伤’的原因。同时当初神兽‘白水泽’也在关键时刻背负着尉迟雪逃命。\n所以纪一川也说，白叔对纪宁有救命之恩。\n父母是在北冥相识、相爱、怀孕。\n‘北冥’一词对纪宁当然有着特殊含义。\n“父亲，母亲。”纪宁郑重道，“这一鞘三剑，我给它取名，就叫北冥剑！”\n******\n在纪宁为获得北冥剑而欢喜时，在燕山这片大地上一处名叫翼蛇湖的地方……\n翼蛇湖，湖泊浩瀚近乎无边，有近百里长宽。\n所谓深山、大湖，必有妖怪。\n这话不假！这一座广阔神秘的大湖毫无疑问是潜伏着大妖，内部小妖更是无数。这湖泽的大妖名为‘翼蛇’，乃是一头活了过千年的老妖，实力滔天，生而能飞行，又能控水、控毒，是一凶威赫赫的大妖。\n在大湖央深处有着一座小岛，正是翼蛇的巢穴所在。\n“吽~~”一头蜿蜒盘踞着的足有数百米长的黑色大蛇，它的两巨大的鳞甲骨翼更是张开着宛如遮天敝地，赤红的瞳孔盯着眼前这一群瑟瑟发抖的妖兽们，一阵阵冰冷的寒气弥漫着，令周围的地面上都是结了一层冰霜。\n密密麻麻的小妖们，一个个或者跪伏，或者趴着，个个瑟瑟发抖。\n有约莫上百名妖兽倒在那全身满是冰霜，已经完全冻毙了。\n“吽~~”愤怒的翼蛇，发出一声声怒吼。\n那些小妖们，各种蛇类、蟹类、鱼类各种狰狞的妖怪们，一个个低声回应着。显然它们一个个都无比恐惧。\n“吼！”翼蛇冰冷的怒吼。\n哗哗哗~~~\n所有的妖们如释重负，个个连飞速退去，许多妖兽们都连离开了小岛进入了深湖。还有部分妖兽则是分散在岛屿上守卫着。\n“嗤~~”那巨大的黑色大蛇忽然化为雾气，紧跟着凝聚而成，化为了一名黑衣男子。\n“我翼，有十二子！”黑衣男子咬牙切齿，“成长就死去大半，活下来的一共才十子！而有神魔血脉的仅仅就一个……我最钟爱的赤芒！”\n蛇性本淫。\n虽然它自己没神魔血脉，可是它和很多后天妖**媾，其也有后天神兽。对于一名修炼过千年的老妖……一些后天神兽自然是手到擒来，可神兽孕育是很少的，他的孩子仅仅一个拥有神魔血脉，便是赤芒。\n也是它最宠爱的，它认定只要赤芒突破为先天生灵，便拥有更加强大的实力，前途将比它还要远大。\n“赤芒，我早说过，在没成为先天生灵前不要出去，人虽然美味，可是吃太多的人，那纪氏就要来讨伐了。”黑衣男子低吼着，痛苦不堪。\n他那骄纵的孩子‘赤芒’，偷偷出去，并且发现人肉的确远超其他妖兽，真是美味。\n赤芒瞒着父亲，一次次出去肆虐。\n“我的孩子，一定得带回来。”黑衣男子顿时化为巨大的翼蛇，骨翼震荡，立即化作黑影破空而去，消失在天边云层。\n——\n星期一冲榜，番茄需要大家的推荐票！\nC"
  }
}
```
