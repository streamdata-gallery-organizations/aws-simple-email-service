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
  /?Action=PutIdentityPolicy&k=1:
    get:
      summary: ' Put Identity Policy '
      description: Adds or updates a sending authorization policy for the specified
        identity (an email address or a domain)
      operationId: putIdentityPolicy
      parameters:
      - in: query
        name: Identity
        description: The identity to which the policy will apply
        type: string
      - in: query
        name: Policy
        description: The text of the policy in JSON format
        type: string
      - in: query
        name: PolicyName
        description: The name of the policy
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