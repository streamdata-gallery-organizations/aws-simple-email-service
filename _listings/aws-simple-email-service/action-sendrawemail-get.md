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
  /?Action=SendRawEmail:
    get:
      summary: ' Send Raw Email '
      description: Sends an email message, with header and content specified by the
        client
      operationId: sendRawEmail
      parameters:
      - in: query
        name: ConfigurationSetName
        description: The name of the configuration set to use when you send an email
          using SendRawEmail
        type: string
      - in: query
        name: Destinations.member.N
        description: 'A list of destinations for the message, consisting of To:, CC:,
          and BCC: addresses'
        type: string
      - in: query
        name: FromArn
        description: This parameter is used only for sending authorization
        type: string
      - in: query
        name: RawMessage
        description: The raw text of the message
        type: string
      - in: query
        name: ReturnPathArn
        description: This parameter is used only for sending authorization
        type: string
      - in: query
        name: Source
        description: The identity's email address
        type: string
      - in: query
        name: SourceArn
        description: This parameter is used only for sending authorization
        type: string
      - in: query
        name: Tags.member.N
        description: A list of tags, in the form of name/value pairs, to apply to
          an email that you send using SendRawEmail
        type: string
      responses:
        200:
          description: OK
      tags:
      - email
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