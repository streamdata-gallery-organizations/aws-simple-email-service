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
  /?Action=ListReceiptFilters:
    get:
      summary: ' List Receipt Filters '
      description: Lists the IP address filters associated with your AWS account
      operationId: listReceiptFilters
      parameters:
      - in: query
        name: Filters.member.N
        description: A list of IP address filter data structures, which each consist
          of a name, an IP address range, and whether to allow or block mail from
          it
        type: string
      responses:
        200:
          description: OK
      tags:
      - receipt filters
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