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
  /?Action=DescribeConfigurationSet:
    get:
      summary: ' Describe Configuration Set '
      description: Returns the details of the specified configuration set
      operationId: describeConfigurationSet
      parameters:
      - in: query
        name: ConfigurationSetAttributeNames.member.N
        description: A list of configuration set attributes to return
        type: string
      - in: query
        name: ConfigurationSetName
        description: The name of the configuration set to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - configuration sets
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