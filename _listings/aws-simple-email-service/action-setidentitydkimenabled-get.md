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
  /?Action=SetIdentityDkimEnabled&k=1:
    get:
      summary: ' Set Identity Dkim Enabled '
      description: |-
        Enables or disables Easy DKIM signing of email sent from an identity:If Easy DKIM
                    signing is enabled for a domain name identity (e
      operationId: setIdentityDkimEnabled
      parameters:
      - in: query
        name: DkimEnabled
        description: Sets whether DKIM signing is enabled for an identity
        type: string
      - in: query
        name: Identity
        description: The identity for which DKIM signing should be enabled or disabled
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