# Get Source Groups
This endpoint returns available source groups

**Request Information**
| Type | URL                 |
| ---- | ------------------- |
| GET  | /source-groups      |

**Query Parameter**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |

**Payload**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |

**Response**
```
{
  groups: [
    {"type": "csv", group: "disneydata"},
    {"type": "csv", group: "googleplay"},
  ]
}
```


**Get Date Range**
This endpoint returns min- and max date of given sources.

**Request Information**
| Type | URL                 |
| ---- | ------------------- |
| GET  | /date-range         |

**Query Parameter**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |
| type                    | str    | true     | always use `group` (will be changed later) |
| q                       | List[str] | true   | groupnames of chosen sources |

**Payload**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |

**Response**
```
{
  min_date: "2020-12-01"
  max_date: "2021-12-13"
}
```


**Create Job**
This endpoint will create a search request if it's not exists.

**Request Information**
| Type | URL                 |
| ---- | ------------------- |
| POST | /create-job         |

**Query Parameter**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |

**Payload**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |
| min_date                | str    | true     | minimum date for job            |
| max_date                | str    | true     | maximum date for job            |
| source_groups           | List[str] | true  | groupnames of chosen sources    |

**Response**
```
{
  id: "abcd-efgh-ijkl-mnopqrs"
}
```
