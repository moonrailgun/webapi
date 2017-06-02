# 追书神器接口文档

## api服务器地址
`http://api.zhuishushenqi.com`

#### 追书架

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
