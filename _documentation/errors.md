---
title: Errors
position: 4
right_code: |
  ~~~ json
  {
    "status": 404,
    "error": "error message here"
  }
  ~~~
  {: title="Error Response" }
---

| Code | Name        | Description                      |
|------|-------------|----------------------------------|
| 400  | Bad Request | We could not process that action |
| 403  | Forbidden   | You exceeded the rate limit      |
| 404  | Not Found   | The requested resource could not be found |
| 500  | Internal Server Error | We had a problem with our server. Please try again later |
| 503  | Service Unavailable   | We are temporarily offline for maintenance. Please try again later |