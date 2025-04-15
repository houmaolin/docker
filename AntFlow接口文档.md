---
title: 个人项目
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.23"

---

# 个人项目

Base URLs:

* <a href="http://localhost:7001">测试环境: http://localhost:7001</a>

# Authentication

# AntFlow

## GET 流程预览/bpmnConf/detail/

GET /bpmnConf/detail/125

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

## GET 待办事项/bpmnConf/todoList

GET /bpmnConf/todoList

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

## POST 流程发布/bpmnConf/edit

POST /bpmnConf/edit

> Body 请求参数

```json
{
  "bpmnCode": "SFZHSQ-00011",
  "bpmnName": "合同审批",
  "bpmnType": null,
  "formCode": "PROJECT_QGkYu4",
  "appId": null,
  "deduplicationType": 2,
  "effectiveStatus": 1,
  "remark": "合同审批",
  "isDel": 0,
  "nodes": [
    {
      "nodeId": "YviYu4",
      "nodeName": "审核人",
      "nodeType": 4,
      "nodeFrom": "IhgYu4",
      "prevId": [],
      "nodeTo": [],
      "setType": 1,
      "directorLevel": 1,
      "signType": 1,
      "noHeaderAction": 1,
      "error": false,
      "property": {
        "emplIds": [
          14
        ],
        "signType": 1
      },
      "nodeProperty": 5
    },
    {
      "nodeId": "IhgYu4",
      "nodeName": "条件1",
      "nodeDisplayName": "园区面积 < 2000",
      "nodeType": 3,
      "nodeFrom": "UcgYu4",
      "prevId": [],
      "nodeTo": [
        "YviYu4"
      ],
      "priorityLevel": 1,
      "nodeApproveList": [],
      "error": false,
      "isDefault": 0,
      "property": {
        "conditionList": [
          {
            "showType": "1",
            "columnId": "3",
            "type": 2,
            "showName": "园区面积",
            "optType": "1",
            "zdy1": "2000",
            "opt1": "<",
            "zdy2": "",
            "opt2": "<",
            "columnDbname": "parkArea",
            "columnType": "Double"
          }
        ],
        "sort": 1,
        "isDefault": 0
      }
    },
    {
      "nodeId": "TkgYu4",
      "nodeName": "条件2",
      "nodeDisplayName": "其他条件进入此流程",
      "nodeType": 3,
      "nodeFrom": "UcgYu4",
      "prevId": [],
      "nodeTo": [],
      "priorityLevel": 2,
      "nodeApproveList": [],
      "isDefault": 1,
      "error": false,
      "property": {
        "conditionList": [],
        "sort": 2,
        "isDefault": 1
      }
    },
    {
      "nodeId": "UcgYu4",
      "nodeName": "路由",
      "nodeType": 2,
      "nodeFrom": "Gb2",
      "prevId": [],
      "nodeTo": [
        "IhgYu4",
        "TkgYu4"
      ],
      "error": true,
      "property": null
    },
    {
      "confId": 35,
      "nodeId": "Gb2",
      "nodeType": 1,
      "nodeProperty": 1,
      "nodePropertyName": null,
      "nodeFrom": "",
      "nodeFroms": null,
      "prevId": [],
      "batchStatus": 0,
      "approvalStandard": 2,
      "nodeName": "发起人",
      "nodeDisplayName": "发起人",
      "annotation": null,
      "isDeduplication": 0,
      "isSignUp": 0,
      "orderedNodeType": null,
      "remark": "",
      "isDel": 0,
      "nodeTo": [
        "UcgYu4"
      ],
      "property": null,
      "params": null,
      "buttons": {
        "startPage": [],
        "approvalPage": [
          2
        ],
        "viewPage": null
      },
      "templateVos": null,
      "approveRemindVo": null,
      "formCode": "PROJECT_uoSXu4",
      "conditionNodes": []
    }
  ]
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|
|body|body|object| 否 |none|
|» bpmnCode|body|string| 是 |none|
|» bpmnName|body|string| 是 |none|
|» bpmnType|body|null| 是 |none|
|» formCode|body|string| 是 |none|
|» appId|body|null| 是 |none|
|» deduplicationType|body|integer| 是 |none|
|» effectiveStatus|body|integer| 是 |none|
|» remark|body|string| 是 |none|
|» isDel|body|integer| 是 |none|
|» nodes|body|[object]| 是 |none|
|»» nodeId|body|string| 是 |none|
|»» nodeName|body|string| 是 |none|
|»» nodeType|body|integer| 是 |none|
|»» nodeFrom|body|string| 是 |none|
|»» prevId|body|[string]| 是 |none|
|»» nodeTo|body|[string]| 是 |none|
|»» setType|body|integer| 否 |none|
|»» directorLevel|body|integer| 否 |none|
|»» signType|body|integer| 否 |none|
|»» noHeaderAction|body|integer| 否 |none|
|»» error|body|boolean| 是 |none|
|»» property|body|object¦null| 是 |none|
|»»» emplIds|body|[integer]| 否 |none|
|»»» signType|body|integer| 否 |none|
|»»» conditionList|body|[object]| 是 |none|
|»»»» showType|body|string| 否 |none|
|»»»» columnId|body|string| 否 |none|
|»»»» type|body|integer| 否 |none|
|»»»» showName|body|string| 否 |none|
|»»»» optType|body|string| 否 |none|
|»»»» zdy1|body|string| 否 |none|
|»»»» opt1|body|string| 否 |none|
|»»»» zdy2|body|string| 否 |none|
|»»»» opt2|body|string| 否 |none|
|»»»» columnDbname|body|string| 否 |none|
|»»»» columnType|body|string| 否 |none|
|»»» sort|body|integer| 是 |none|
|»»» isDefault|body|integer| 是 |none|
|»» nodeProperty|body|integer| 是 |none|
|»» nodeDisplayName|body|string| 是 |none|
|»» priorityLevel|body|integer| 是 |none|
|»» nodeApproveList|body|[string]| 是 |none|
|»» isDefault|body|integer| 是 |none|
|»» confId|body|integer| 否 |none|
|»» nodePropertyName|body|null| 否 |none|
|»» nodeFroms|body|null| 否 |none|
|»» batchStatus|body|integer| 否 |none|
|»» approvalStandard|body|integer| 否 |none|
|»» annotation|body|null| 否 |none|
|»» isDeduplication|body|integer| 否 |none|
|»» isSignUp|body|integer| 否 |none|
|»» orderedNodeType|body|null| 否 |none|
|»» remark|body|string| 否 |none|
|»» isDel|body|integer| 否 |none|
|»» params|body|null| 否 |none|
|»» buttons|body|object| 否 |none|
|»»» startPage|body|[string]| 是 |none|
|»»» approvalPage|body|[integer]| 是 |none|
|»»» viewPage|body|null| 是 |none|
|»» templateVos|body|null| 否 |none|
|»» approveRemindVo|body|null| 否 |none|
|»» formCode|body|string| 否 |none|
|»» conditionNodes|body|[string]| 否 |none|

> 返回示例

```json
{
  "requestId": "GB6rhdoN21KaX0BoVoP_15",
  "code": 200,
  "data": null,
  "success": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|null|true|none||none|
|» data|null|true|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|string|true|none||none|
|» errCode|string|true|none||none|
|» errMsg|string|true|none||none|

## POST 代办列表/bpmnConf/process/listPage

POST /bpmnConf/process/listPage/5

> Body 请求参数

```json
{
  "pageDto": {},
  "taskMgmtVO": {}
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## POST 已办列表/bpmnConf/process/listPage

POST /bpmnConf/process/listPage/4

> Body 请求参数

```json
{
  "pageDto": {},
  "taskMgmtVO": {}
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## POST 我的发起列表/bpmnConf/process/listPage

POST /bpmnConf/process/listPage/3

> Body 请求参数

```json
{
  "pageDto": {},
  "taskMgmtVO": {}
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## POST 所有实例列表/bpmnConf/process/listPage

POST /bpmnConf/process/listPage/6

> Body 请求参数

```json
{
  "pageDto": {
    "page": 1,
    "pageSize": 10
  },
  "taskMgmtVO": {}
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## POST 委托列表 /bpmnBusiness/entrustList

POST /bpmnBusiness/entrustlist/1

> Body 请求参数

```json
{
  "pageDto": {
    "page": 1,
    "pageSize": 10
  },
  "taskMgmtVO": {}
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## POST 设置委托  /bpmnBusiness/editEntrust

POST /bpmnBusiness/editEntrust

> Body 请求参数

```json
{
  "ids": [
    {
      "id": 0,
      "powerId": 10
    }
  ],
  "sender": 1,
  "receiverId": 2,
  "receiverName": "李四",
  "beginTime": "",
  "endTime": ""
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## GET 设置委托  /bpmnBusiness/entrustDetail

GET /bpmnBusiness/entrustDetail/1

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userid|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{
  "data": [
    {
      "taskId": "string",
      "taskName": "string",
      "processInstanceId": "string",
      "processKey": "string",
      "createTime": "string",
      "description": "string",
      "runTime": "string",
      "actualName": "string",
      "processNumber": "string",
      "taskState": "string",
      "taskStype": 0,
      "processState": 0,
      "businessId": 0,
      "processTypeName": "string",
      "nodeType": 0,
      "userId": 0,
      "isLeftStroke": true,
      "title": "string",
      "isBatchSubmit": true,
      "isForward": true,
      "processCode": "string",
      "processDigest": "string"
    }
  ],
  "pagination": {
    "page": 0,
    "pageSize": 0,
    "totalCount": 0,
    "pageCount": 0,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null
  },
  "statistics": null,
  "sortColumnMap": null,
  "flag": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» data|[object]|true|none||none|
|»» taskId|string|true|none||none|
|»» taskName|string|true|none||none|
|»» processInstanceId|string|true|none||none|
|»» processKey|string|true|none||none|
|»» createTime|string|true|none||none|
|»» description|string|true|none||none|
|»» runTime|string|true|none||none|
|»» actualName|string|true|none||none|
|»» processNumber|string|true|none||none|
|»» taskState|string|true|none||none|
|»» taskStype|integer|true|none||none|
|»» processState|integer|true|none||none|
|»» businessId|integer|true|none||none|
|»» processTypeName|string|true|none||none|
|»» nodeType|integer|true|none||none|
|»» userId|integer|true|none||none|
|»» isLeftStroke|boolean|true|none||none|
|»» title|string|true|none||none|
|»» isBatchSubmit|boolean|true|none||none|
|»» isForward|boolean|true|none||none|
|»» processCode|string|true|none||none|
|»» processDigest|string|true|none||none|
|» pagination|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|integer|true|none||none|
|»» pageCount|integer|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|» statistics|null|true|none||none|
|» sortColumnMap|null|true|none||none|
|» flag|null|true|none||none|

## GET 获取FromCode/-/bpmnBusiness/listFormCodes

GET /bpmnBusiness/listFormCodes

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{
  "requestId": "string",
  "code": 0,
  "data": [
    "string"
  ],
  "success": true,
  "needRetry": true,
  "expInfo": null,
  "errCode": null,
  "errMsg": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|integer|true|none||none|
|» data|[string]|true|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|null|true|none||none|
|» errCode|null|true|none||none|
|» errMsg|null|true|none||none|

## GET 获取FromCode-KV/-/bpmnBusiness/listFormInfo

GET /bpmnBusiness/listFormInfo

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{
  "requestId": "string",
  "code": 0,
  "data": [
    {
      "key": "string",
      "value": "string"
    }
  ],
  "success": true,
  "needRetry": true,
  "expInfo": null,
  "errCode": null,
  "errMsg": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|integer|true|none||none|
|» data|[object]|true|none||none|
|»» key|string|false|none||none|
|»» value|string|false|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|null|true|none||none|
|» errCode|null|true|none||none|
|» errMsg|null|true|none||none|

## GET 流程生效/bpmnConf/effectiveBpmn/id

GET /bpmnConf/effectiveBpmn/125

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{
  "requestId": "string",
  "code": 0,
  "data": null,
  "success": true,
  "needRetry": true,
  "expInfo": null,
  "errCode": null,
  "errMsg": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|integer|true|none||none|
|» data|null|true|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|null|true|none||none|
|» errCode|null|true|none||none|
|» errMsg|null|true|none||none|

## POST 流程详情/bpmnConf/process/viewBusinessProcess

POST /bpmnConf/process/viewBusinessProcess

> Body 请求参数

```json
{
  "formCode": "DSFZH_WMA",
  "processKey": "DSFZH_WMA",
  "processNumber": "DSFZH_WMA_23",
  "type": 2
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "requestId": "string",
  "code": 0,
  "data": {
    "page": 0,
    "pageSize": 0,
    "totalCount": null,
    "pageCount": null,
    "startIndex": 0,
    "orderColumn": null,
    "orderType": null,
    "processNumber": "string",
    "processKey": "string",
    "businessId": 0,
    "params": null,
    "processTitle": null,
    "approvalComment": null,
    "entityName": null,
    "processRecordInfo": {
      "verifyInfoList": [
        {
          "id": 0,
          "verifyUserName": "string",
          "verifyStatus": 0,
          "verifyDesc": "string",
          "verifyDate": "string",
          "taskName": "string",
          "verifyStatusName": "string"
        }
      ],
      "processTitle": "string",
      "processNumber": "string",
      "startUserId": "string",
      "createTime": "string",
      "taskState": "string",
      "pcButtons": {
        "initiate": [
          "string"
        ],
        "audit": [
          "string"
        ],
        "toView": [
          "string"
        ]
      }
    },
    "type": null,
    "processState": true,
    "taskId": null,
    "objectMap": null,
    "moreHandlers": null,
    "formCode": "string",
    "operationType": null,
    "userIds": null,
    "approversList": null,
    "flag": null,
    "initDatas": null,
    "isShowSalary": null,
    "startUserId": "string",
    "bpmnCode": null,
    "bpmnName": null,
    "emplId": null,
    "paramStr": null,
    "empId": null,
    "processDigest": null,
    "dataSourceId": null,
    "empIds": null,
    "isSignUpNode": true,
    "signUpUsers": null,
    "isStartPagePreview": null,
    "backToEmployeeId": null,
    "formData": null,
    "bpmnConfVo": null,
    "accountType": 0,
    "jobLevelVo": null,
    "assignee": null,
    "remark": "string",
    "accountOwnerName": null
  },
  "success": true,
  "needRetry": true,
  "expInfo": null,
  "errCode": null,
  "errMsg": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|integer|true|none||none|
|» data|object|true|none||none|
|»» page|integer|true|none||none|
|»» pageSize|integer|true|none||none|
|»» totalCount|null|true|none||none|
|»» pageCount|null|true|none||none|
|»» startIndex|integer|true|none||none|
|»» orderColumn|null|true|none||none|
|»» orderType|null|true|none||none|
|»» processNumber|string|true|none||none|
|»» processKey|string|true|none||none|
|»» businessId|integer|true|none||none|
|»» params|null|true|none||none|
|»» processTitle|null|true|none||none|
|»» approvalComment|null|true|none||none|
|»» entityName|null|true|none||none|
|»» processRecordInfo|object|true|none||none|
|»»» verifyInfoList|[object]|true|none||none|
|»»»» id|integer|true|none||none|
|»»»» verifyUserName|string|true|none||none|
|»»»» verifyStatus|integer|true|none||none|
|»»»» verifyDesc|string|true|none||none|
|»»»» verifyDate|string|true|none||none|
|»»»» taskName|string|true|none||none|
|»»»» verifyStatusName|string|true|none||none|
|»»» processTitle|string|true|none||none|
|»»» processNumber|string|true|none||none|
|»»» startUserId|string|true|none||none|
|»»» createTime|string|true|none||none|
|»»» taskState|string|true|none||none|
|»»» pcButtons|object|true|none||none|
|»»»» initiate|[string]|true|none||none|
|»»»» audit|[string]|true|none||none|
|»»»» toView|[string]|true|none||none|
|»» type|null|true|none||none|
|»» processState|boolean|true|none||none|
|»» taskId|null|true|none||none|
|»» objectMap|null|true|none||none|
|»» moreHandlers|null|true|none||none|
|»» formCode|string|true|none||none|
|»» operationType|null|true|none||none|
|»» userIds|null|true|none||none|
|»» approversList|null|true|none||none|
|»» flag|null|true|none||none|
|»» initDatas|null|true|none||none|
|»» isShowSalary|null|true|none||none|
|»» startUserId|string|true|none||none|
|»» bpmnCode|null|true|none||none|
|»» bpmnName|null|true|none||none|
|»» emplId|null|true|none||none|
|»» paramStr|null|true|none||none|
|»» empId|null|true|none||none|
|»» processDigest|null|true|none||none|
|»» dataSourceId|null|true|none||none|
|»» empIds|null|true|none||none|
|»» isSignUpNode|boolean|true|none||none|
|»» signUpUsers|null|true|none||none|
|»» isStartPagePreview|null|true|none||none|
|»» backToEmployeeId|null|true|none||none|
|»» formData|null|true|none||none|
|»» bpmnConfVo|null|true|none||none|
|»» accountType|integer|true|none||none|
|»» jobLevelVo|null|true|none||none|
|»» assignee|null|true|none||none|
|»» remark|string|true|none||none|
|»» accountOwnerName|null|true|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|null|true|none||none|
|» errCode|null|true|none||none|
|» errMsg|null|true|none||none|

## GET 配置审批人/bpmnBusiness/listNodeProperties

GET /bpmnBusiness/listNodeProperties

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

## POST 流程配置列表/bpmnConf/listPage

POST /bpmnConf/listPage

> Body 请求参数

```json
{
  "pageDto": {
    "page": 1,
    "pageSize": 10
  },
  "entity": {}
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

## POST 发起/bpmnConf/process/buttonsOperation

POST /bpmnConf/process/buttonsOperation

> Body 请求参数

```json
{
  "formCode": "DSFZH_WMA",
  "operationType": 1,
  "accountType": 1,
  "remark": "发起测试流程accountType11"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|formCode|query|string| 否 |none|
|userId|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "requestId": "string",
  "code": null,
  "data": null,
  "success": true,
  "needRetry": true,
  "expInfo": "string",
  "errCode": "string",
  "errMsg": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|null|true|none||none|
|» data|null|true|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|string|true|none||none|
|» errCode|string|true|none||none|
|» errMsg|string|true|none||none|

## GET 审批进度bpmnConf/getBpmVerifyInfoVos

GET /bpmnConf/getBpmVerifyInfoVos

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|processNumber|query|string| 否 |none|
|userId|header|string| 否 |none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

## POST 流程预览ByBpmnCode /startPagePreviewNode

POST /bpmnConf/startPagePreviewNode

> Body 请求参数

```json
{
  "processNumber": "LEAVE_WMA_17",
  "isStartPreview": false
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|UserId|header|string| 否 |none|
|body|body|object| 否 |none|

> 返回示例

> 200 Response

```json
{
  "requestId": "string",
  "code": 0,
  "data": {
    "bpmnName": "string",
    "formCode": "string",
    "bpmnNodeList": [
      {
        "id": 0,
        "confId": 0,
        "nodeId": "string",
        "nodeType": 0,
        "nodeProperty": 0,
        "nodePropertyName": "string",
        "nodeFrom": "string",
        "nodeFroms": null,
        "prevId": [
          "string"
        ],
        "batchStatus": 0,
        "approvalStandard": 0,
        "nodeName": "string",
        "nodeDisplayName": "string",
        "annotation": null,
        "isDeduplication": 0,
        "deduplicationExclude": true,
        "isSignUp": 0,
        "orderedNodeType": null,
        "remark": "string",
        "isDel": 0,
        "createUser": "string",
        "createTime": "string",
        "updateUser": "string",
        "updateTime": "string",
        "nodeTo": [
          "string"
        ],
        "property": {
          "loopEndType": null,
          "loopNumberPlies": null,
          "loopEndGrade": null,
          "loopEndPersonList": null,
          "loopEndPersonObjList": null,
          "assignLevelType": null,
          "assignLevelGrade": null,
          "hrbpConfType": null,
          "roleIds": null,
          "roleList": null,
          "emplIds": [
            null
          ],
          "emplList": [
            null
          ],
          "signType": 0,
          "conditionsConf": null,
          "conditionList": null,
          "configurationTableType": null,
          "tableFieldType": null,
          "isMultiPeople": null,
          "noparticipatingStaffIds": null,
          "noparticipatingStaffs": null,
          "functionId": null,
          "functionName": null,
          "afterSignUpWay": null,
          "signUpType": null,
          "nodeMark": null,
          "isDefault": null,
          "sort": null
        },
        "params": {
          "nodeTo": "string",
          "paramType": 0,
          "assignee": {},
          "assigneeList": [
            null
          ],
          "isNodeDeduplication": 0
        },
        "buttons": {
          "startPage": [
            null
          ],
          "approvalPage": [
            null
          ],
          "viewPage": null
        },
        "templateVos": null,
        "approveRemindVo": null,
        "conditionsUrl": null,
        "formCode": "string"
      }
    ],
    "startUserInfo": null,
    "employeeInfo": null,
    "deduplicationType": 0,
    "deduplicationTypeName": "string"
  },
  "success": true,
  "needRetry": true,
  "expInfo": null,
  "errCode": null,
  "errMsg": null
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» requestId|string|true|none||none|
|» code|integer|true|none||none|
|» data|object|true|none||none|
|»» bpmnName|string|true|none||none|
|»» formCode|string|true|none||none|
|»» bpmnNodeList|[object]|true|none||none|
|»»» id|integer|true|none||none|
|»»» confId|integer|true|none||none|
|»»» nodeId|string|true|none||none|
|»»» nodeType|integer|true|none||none|
|»»» nodeProperty|integer|true|none||none|
|»»» nodePropertyName|string¦null|true|none||none|
|»»» nodeFrom|string|true|none||none|
|»»» nodeFroms|null|true|none||none|
|»»» prevId|[string]|true|none||none|
|»»» batchStatus|integer|true|none||none|
|»»» approvalStandard|integer|true|none||none|
|»»» nodeName|string|true|none||none|
|»»» nodeDisplayName|string|true|none||none|
|»»» annotation|null|true|none||none|
|»»» isDeduplication|integer|true|none||none|
|»»» deduplicationExclude|boolean|true|none||none|
|»»» isSignUp|integer|true|none||none|
|»»» orderedNodeType|null|true|none||none|
|»»» remark|string|true|none||none|
|»»» isDel|integer|true|none||none|
|»»» createUser|string|true|none||none|
|»»» createTime|string|true|none||none|
|»»» updateUser|string|true|none||none|
|»»» updateTime|string|true|none||none|
|»»» nodeTo|[string]¦null|true|none||none|
|»»» property|object|true|none||none|
|»»»» loopEndType|null|true|none||none|
|»»»» loopNumberPlies|null|true|none||none|
|»»»» loopEndGrade|null|true|none||none|
|»»»» loopEndPersonList|null|true|none||none|
|»»»» loopEndPersonObjList|null|true|none||none|
|»»»» assignLevelType|null|true|none||none|
|»»»» assignLevelGrade|null|true|none||none|
|»»»» hrbpConfType|null|true|none||none|
|»»»» roleIds|null|true|none||none|
|»»»» roleList|null|true|none||none|
|»»»» emplIds|[string]|true|none||none|
|»»»» emplList|[object]|true|none||none|
|»»»»» id|integer|false|none||none|
|»»»»» name|string|false|none||none|
|»»»» signType|integer|true|none||none|
|»»»» conditionsConf|null|true|none||none|
|»»»» conditionList|null|true|none||none|
|»»»» configurationTableType|null|true|none||none|
|»»»» tableFieldType|null|true|none||none|
|»»»» isMultiPeople|null|true|none||none|
|»»»» noparticipatingStaffIds|null|true|none||none|
|»»»» noparticipatingStaffs|null|true|none||none|
|»»»» functionId|null|true|none||none|
|»»»» functionName|null|true|none||none|
|»»»» afterSignUpWay|null|true|none||none|
|»»»» signUpType|null|true|none||none|
|»»»» nodeMark|null|true|none||none|
|»»»» isDefault|null|true|none||none|
|»»»» sort|null|true|none||none|
|»»» params|object|true|none||none|
|»»»» nodeTo|string¦null|true|none||none|
|»»»» paramType|integer|true|none||none|
|»»»» assignee|object¦null|true|none||none|
|»»»»» assignee|string|true|none||none|
|»»»»» assigneeName|null|true|none||none|
|»»»»» elementName|string|true|none||none|
|»»»»» isDeduplication|integer|true|none||none|
|»»»» assigneeList|[object]|true|none||none|
|»»»»» assignee|string|true|none||none|
|»»»»» assigneeName|string¦null|true|none||none|
|»»»»» elementName|string|true|none||none|
|»»»»» isDeduplication|integer|true|none||none|
|»»»» isNodeDeduplication|integer|true|none||none|
|»»» buttons|object|true|none||none|
|»»»» startPage|[integer]|true|none||none|
|»»»» approvalPage|[integer]|true|none||none|
|»»»» viewPage|null|true|none||none|
|»»» templateVos|null|true|none||none|
|»»» approveRemindVo|null|true|none||none|
|»»» conditionsUrl|null|true|none||none|
|»»» formCode|string|true|none||none|
|»» startUserInfo|null|true|none||none|
|»» employeeInfo|null|true|none||none|
|»» deduplicationType|integer|true|none||none|
|»» deduplicationTypeName|string|true|none||none|
|» success|boolean|true|none||none|
|» needRetry|boolean|true|none||none|
|» expInfo|null|true|none||none|
|» errCode|null|true|none||none|
|» errMsg|null|true|none||none|
 