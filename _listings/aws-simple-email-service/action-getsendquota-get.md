---
swagger: "2.0"
info:
  title: AWS Simple Email Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetSendQuota:
    get:
      summary: ' Get Send Quota '
      description: Returns the user's current sending limits
      operationId: getSendQuota
      parameters:
      - in: query
        name: Max24HourSend
        description: The maximum number of emails the user is allowed to send in a
          24-hour interval
        type: string
      - in: query
        name: MaxSendRate
        description: The maximum number of emails that Amazon SES can accept from
          the user's account per second
        type: string
      - in: query
        name: SentLast24Hours
        description: The number of emails sent during the previous 24 hours
        type: string
      responses:
        200:
          description: OK
      tags:
      - send quota
definitions: []
x-collection-name: AWS Simple Email Service
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---