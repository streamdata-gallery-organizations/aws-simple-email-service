---
swagger: "2.0"
x-collection-name: AWS Simple Email Service
x-complete: 0
info:
  title: AWS Simple Email Service API Create Receipt Rule
  version: 1.0.0
  description: Creates a receipt rule.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CloneReceiptRuleSet:
    get:
      summary: Clone Receipt Rule Set
      description: Creates a receipt rule set by cloning an existing one.
      operationId: cloneReceiptRuleSet
      x-api-path-slug: actionclonereceiptruleset-get
      parameters:
      - in: query
        name: OriginalRuleSetName
        description: The name of the rule set to clone
        type: string
      - in: query
        name: RuleSetName
        description: The name of the rule set to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=CreateConfigurationSet:
    get:
      summary: Create Configuration Set
      description: Creates a configuration set.
      operationId: createConfigurationSet
      x-api-path-slug: actioncreateconfigurationset-get
      parameters:
      - in: query
        name: ConfigurationSet
        description: A data structure that contains the name of the configuration
          set
        type: string
      responses:
        200:
          description: OK
      tags:
      - Configuration Sets
  /?Action=CreateConfigurationSetEventDestination:
    get:
      summary: Create Configuration Set Event Destination
      description: Creates a configuration set event destination.
      operationId: createConfigurationSetEventDestination
      x-api-path-slug: actioncreateconfigurationseteventdestination-get
      parameters:
      - in: query
        name: ConfigurationSetName
        description: The name of the configuration set to which to apply the event
          destination
        type: string
      - in: query
        name: EventDestination
        description: An object that describes the AWS service to which Amazon SES
          will publish the email sending events associated with the specified configuration
          set
        type: string
      responses:
        200:
          description: OK
      tags:
      - Configuration Set Event Destination
  /?Action=CreateReceiptFilter:
    get:
      summary: Create Receipt Filter
      description: Creates a new IP address filter.
      operationId: createReceiptFilter
      x-api-path-slug: actioncreatereceiptfilter-get
      parameters:
      - in: query
        name: Filter
        description: A data structure that describes the IP address filter to create,
          which consists of a name, an IP address range, and whether to allow or block
          mail from it
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Filters
  /?Action=CreateReceiptRule:
    get:
      summary: Create Receipt Rule
      description: Creates a receipt rule.
      operationId: createReceiptRule
      x-api-path-slug: actioncreatereceiptrule-get
      parameters:
      - in: query
        name: After
        description: The name of an existing rule after which the new rule will be
          placed
        type: string
      - in: query
        name: Rule
        description: A data structure that contains the specified rules name, actions,
          recipients, domains, enabled status, scan status, and TLS policy
        type: string
      - in: query
        name: RuleSetName
        description: The name of the rule set to which to add the rule
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rules
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