# Get Source Groups
This endpoint returns available source groups

**Request Information**
| Type | URL                 |
| ---- | ------------------- |
| GET  | /get_sources        |
| GET  | /source-groups (expired)      |

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
    {"review_count": 1005, "source_type": "csv", "group": "disney"},
    {"review_count": 985, "source_type": "csv", "group": "googleplay"}
  ]
}
```


# Get Date Range
This endpoint returns min- and max date of given sources.

**Request Information**
| Type | URL                 |
| ---- | ------------------- |
| GET  | /get_source_date_range         |
| GET  | /date-range (expired)         |

**Query Parameter**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |
| group                   | List[str] | true  | List of selected group names    |
| source_type             | List[str] | true  | List of selected source types   |

**Payload**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |

**Response**
```
{
  "review_count": 1005,
  "min_date": "2017-06-01",
  "max_date": "2019-05-01"
}
```


# Get Review Count
This endpoint returns count of reviews for given filter options

**Request Information**
| Type | URL                 |
| ---- | ------------------- |
| GET  | /get_review_count   |

**Query Parameter**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |
| group                   | List[str] | true  | List of selected group names    |
| source_type             | List[str] | true  | List of selected source types   |
| min_date                | str       | true  | minimum date (included). Format %Y-%m-%d   |
| max_date                | str       | true  | maximum date (excluded). Format %Y-%m-%d   |

**Payload**
| Property Name           | type   | required | Description                     |
| ----------------------- | ------ | -------- | ------------------------------- |

**Response**
```
{
  "review_count": 1005
}
```


# Create Job
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
