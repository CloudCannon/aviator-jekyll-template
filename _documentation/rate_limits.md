---
title: Rate Limits
position: 3
right_code: |
  ~~~ http
  HTTP/1.1 403 Forbidden
  Date: Mon, 21 Apr 2014 13:26:48 GMT
  Content-Type: application/json; charset=utf-8
  {
    "message": "Rate Limit Exceeded"
  }
  ~~~
  {: title="Error When Rate Limit Exceeded" }
---

#### Overview

Rate limits are enforced for all third-party applications and services. This document is an overview of the rate limits themselves, as well as how they are enforced and best practices for handling the errors returned when a rate limit is reached.

Third-party applications are currently throttled to 5000 requests per hour. As this API continues to age, the rate limits may be updated to provide better performance to users

#### Rationale

As previously mentioned, the primary goal is to provide a responsive interface for developers and users to use when accessing the MTG data. Since each request made to the API incurs a computational cost, it’s in the best interest of both Magic: The Gathering API and its developer partners that these costs be minimized to the greatest degree possible.

Rate limiting also helps third-party developers by encouraging them to build their integrations to make economical use of API requests.