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
  /?Action=ListIdentities&k=1:
    get:
      summary: ' List Identities '
      description: Returns a list containing all of the identities (email addresses
        and domains) for your AWS account, regardless of verification status
      operationId: listIdentities
      parameters:
      - in: query
        name: IdentityType
        description: The type of the identities to list
        type: string
      - in: query
        name: MaxItems
        description: The maximum number of identities per page
        type: string
      - in: query
        name: NextToken
        description: The token to use for pagination
        type: string
      responses:
        200:
          description: OK
      tags:
      - identity
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