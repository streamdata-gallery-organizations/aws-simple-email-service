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
  /?Action=SendEmail&k=1:
    get:
      summary: ' Send Email '
      description: Composes an email message based on input data, and then immediately
        queues the message for sending
      operationId: sendEmail
      parameters:
      - in: query
        name: ConfigurationSetName
        description: The name of the configuration set to use when you send an email
          using SendEmail
        type: string
      - in: query
        name: Destination
        description: 'The destination for this email, composed of To:, CC:, and BCC:
          fields'
        type: string
      - in: query
        name: Message
        description: The message to be sent
        type: string
      - in: query
        name: ReplyToAddresses.member.N
        description: The reply-to email address(es) for the message
        type: string
      - in: query
        name: ReturnPath
        description: The email address to which bounces and complaints are to be forwarded
          when feedback forwarding is enabled
        type: string
      - in: query
        name: ReturnPathArn
        description: This parameter is used only for sending authorization
        type: string
      - in: query
        name: Source
        description: The email address that is sending the email
        type: string
      - in: query
        name: SourceArn
        description: This parameter is used only for sending authorization
        type: string
      - in: query
        name: Tags.member.N
        description: A list of tags, in the form of name/value pairs, to apply to
          an email that you send using SendEmail
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