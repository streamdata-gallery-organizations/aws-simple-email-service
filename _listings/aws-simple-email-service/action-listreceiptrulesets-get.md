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
  /?Action=ListReceiptRuleSets&k=1:
    get:
      summary: ' List Receipt Rule Sets '
      description: Lists the receipt rule sets that exist under your AWS account
      operationId: listReceiptRuleSets
      parameters:
      - in: query
        name: NextToken
        description: A token returned from a previous call to ListReceiptRuleSets
          to indicate the position in the receipt rule set list
        type: string
      responses:
        200:
          description: OK
      tags:
      - receipt rule sets
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