---
swagger: "2.0"
x-collection-name: AWS Simple Email Service
x-complete: 0
info:
  title: AWS Simple Email Service API Set Identity Feedback Forwarding Enabled
  version: 1.0.0
  description: Given an identity (an email address or a domain), enables or disables
    whether Amazon SES forwards bounce and complaint notifications as email.
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
  /?Action=CreateReceiptRuleSet:
    get:
      summary: Create Receipt Rule Set
      description: Creates an empty receipt rule set.
      operationId: createReceiptRuleSet
      x-api-path-slug: actioncreatereceiptruleset-get
      parameters:
      - in: query
        name: RuleSetName
        description: The name of the rule set to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=DeleteConfigurationSet:
    get:
      summary: Delete Configuration Set
      description: Deletes a configuration set.
      operationId: deleteConfigurationSet
      x-api-path-slug: actiondeleteconfigurationset-get
      parameters:
      - in: query
        name: ConfigurationSetName
        description: The name of the configuration set to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Configuration Sets
  /?Action=DeleteConfigurationSetEventDestination:
    get:
      summary: Delete Configuration Set Event Destination
      description: Deletes a configuration set event destination.
      operationId: deleteConfigurationSetEventDestination
      x-api-path-slug: actiondeleteconfigurationseteventdestination-get
      parameters:
      - in: query
        name: ConfigurationSetName
        description: The name of the configuration set from which to delete the event
          destination
        type: string
      - in: query
        name: EventDestinationName
        description: The name of the event destination to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Configuration Set Event Destination
  /?Action=DeleteIdentity:
    get:
      summary: Delete Identity
      description: Deletes the specified identity (an email address or a domain) from
        the list of verified identities.
      operationId: deleteIdentity
      x-api-path-slug: actiondeleteidentity-get
      parameters:
      - in: query
        name: Identity
        description: The identity to be removed from the list of identities for the
          AWS Account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=DeleteIdentityPolicy:
    get:
      summary: Delete Identity Policy
      description: Deletes the specified sending authorization policy for the given
        identity (an email address or a domain).
      operationId: deleteIdentityPolicy
      x-api-path-slug: actiondeleteidentitypolicy-get
      parameters:
      - in: query
        name: Identity
        description: The identity that is associated with the policy that you want
          to delete
        type: string
      - in: query
        name: PolicyName
        description: The name of the policy to be deleted
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=DeleteReceiptFilter:
    get:
      summary: Delete Receipt Filter
      description: Deletes the specified IP address filter.
      operationId: deleteReceiptFilter
      x-api-path-slug: actiondeletereceiptfilter-get
      parameters:
      - in: query
        name: FilterName
        description: The name of the IP address filter to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Filters
  /?Action=DeleteReceiptRule:
    get:
      summary: Delete Receipt Rule
      description: Deletes the specified receipt rule.
      operationId: deleteReceiptRule
      x-api-path-slug: actiondeletereceiptrule-get
      parameters:
      - in: query
        name: RuleName
        description: The name of the receipt rule to delete
        type: string
      - in: query
        name: RuleSetName
        description: The name of the receipt rule set that contains the receipt rule
          to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rules
  /?Action=DeleteReceiptRuleSet:
    get:
      summary: Delete Receipt Rule Set
      description: Deletes the specified receipt rule set and all of the receipt rules
        it contains.
      operationId: deleteReceiptRuleSet
      x-api-path-slug: actiondeletereceiptruleset-get
      parameters:
      - in: query
        name: RuleSetName
        description: The name of the receipt rule set to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=DeleteVerifiedEmailAddress:
    get:
      summary: Delete Verified Email Address
      description: Deletes the specified email address from the list of verified addresses.
      operationId: deleteVerifiedEmailAddress
      x-api-path-slug: actiondeleteverifiedemailaddress-get
      parameters:
      - in: query
        name: EmailAddress
        description: An email address to be removed from the list of verified addresses
        type: string
      responses:
        200:
          description: OK
      tags:
      - Verified Email Addresses
  /?Action=DescribeActiveReceiptRuleSet:
    get:
      summary: Describe Active Receipt Rule Set
      description: Returns the metadata and receipt rules for the receipt rule set
        that is currently active.
      operationId: describeActiveReceiptRuleSet
      x-api-path-slug: actiondescribeactivereceiptruleset-get
      parameters:
      - in: query
        name: Metadata
        description: The metadata for the currently active receipt rule set
        type: string
      - in: query
        name: Rules.member.N
        description: The receipt rules that belong to the active rule set
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=DescribeConfigurationSet:
    get:
      summary: Describe Configuration Set
      description: Returns the details of the specified configuration set.
      operationId: describeConfigurationSet
      x-api-path-slug: actiondescribeconfigurationset-get
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
      - Configuration Sets
  /?Action=DescribeReceiptRule:
    get:
      summary: Describe Receipt Rule
      description: Returns the details of the specified receipt rule.
      operationId: describeReceiptRule
      x-api-path-slug: actiondescribereceiptrule-get
      parameters:
      - in: query
        name: RuleName
        description: The name of the receipt rule
        type: string
      - in: query
        name: RuleSetName
        description: The name of the receipt rule set to which the receipt rule belongs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rules
  /?Action=DescribeReceiptRuleSet:
    get:
      summary: Describe Receipt Rule Set
      description: Returns the details of the specified receipt rule set.
      operationId: describeReceiptRuleSet
      x-api-path-slug: actiondescribereceiptruleset-get
      parameters:
      - in: query
        name: RuleSetName
        description: The name of the receipt rule set to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=GetIdentityDkimAttributes:
    get:
      summary: Get Identity Dkim Attributes
      description: Returns the current status of Easy DKIM signing for an entity.
      operationId: getIdentityDkimAttributes
      x-api-path-slug: actiongetidentitydkimattributes-get
      parameters:
      - in: query
        name: Identities.member.N
        description: A list of one or more verified identities - email addresses,
          domains, or both
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=GetIdentityMailFromDomainAttributes:
    get:
      summary: Get Identity Mail From Domain Attributes
      description: Returns the custom MAIL FROM attributes for a list of identities
        (email addresses and/or domains).
      operationId: getIdentityMailFromDomainAttributes
      x-api-path-slug: actiongetidentitymailfromdomainattributes-get
      parameters:
      - in: query
        name: Identities.member.N
        description: A list of one or more identities
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=GetIdentityNotificationAttributes:
    get:
      summary: Get Identity Notification Attributes
      description: Given a list of verified identities (email addresses and/or domains),
        returns a structure describing identity notification attributes.
      operationId: getIdentityNotificationAttributes
      x-api-path-slug: actiongetidentitynotificationattributes-get
      parameters:
      - in: query
        name: Identities.member.N
        description: A list of one or more identities
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=GetIdentityPolicies:
    get:
      summary: Get Identity Policies
      description: Returns the requested sending authorization policies for the given
        identity (an email address or a domain).
      operationId: getIdentityPolicies
      x-api-path-slug: actiongetidentitypolicies-get
      parameters:
      - in: query
        name: Identity
        description: The identity for which the policies will be retrieved
        type: string
      - in: query
        name: PolicyNames.member.N
        description: A list of the names of policies to be retrieved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=GetIdentityVerificationAttributes:
    get:
      summary: Get Identity Verification Attributes
      description: Given a list of identities (email addresses and/or domains), returns
        the verification status and (for domain identities) the verification token
        for each identity.
      operationId: getIdentityVerificationAttributes
      x-api-path-slug: actiongetidentityverificationattributes-get
      parameters:
      - in: query
        name: Identities.member.N
        description: A list of identities
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=GetSendQuota:
    get:
      summary: Get Send Quota
      description: Returns the user's current sending limits.
      operationId: getSendQuota
      x-api-path-slug: actiongetsendquota-get
      parameters:
      - in: query
        name: Max24HourSend
        description: The maximum number of emails the user is allowed to send in a
          24-hour interval
        type: string
      - in: query
        name: MaxSendRate
        description: The maximum number of emails that Amazon SES can accept from
          the users account per second
        type: string
      - in: query
        name: SentLast24Hours
        description: The number of emails sent during the previous 24 hours
        type: string
      responses:
        200:
          description: OK
      tags:
      - Send Quota
  /?Action=GetSendStatistics:
    get:
      summary: Get Send Statistics
      description: Returns the user's sending statistics.
      operationId: getSendStatistics
      x-api-path-slug: actiongetsendstatistics-get
      parameters:
      - in: query
        name: SendDataPoints.member.N
        description: A list of data points, each of which represents 15 minutes of
          activity
        type: string
      responses:
        200:
          description: OK
      tags:
      - Send Statistics
  /?Action=ListConfigurationSets:
    get:
      summary: List Configuration Sets
      description: Lists the configuration sets associated with your AWS account.
      operationId: listConfigurationSets
      x-api-path-slug: actionlistconfigurationsets-get
      parameters:
      - in: query
        name: MaxItems
        description: The number of configuration sets to return
        type: string
      - in: query
        name: NextToken
        description: A token returned from a previous call to ListConfigurationSets
          to indicate the position of the configuration set in the configuration set
          list
        type: string
      responses:
        200:
          description: OK
      tags:
      - Configuration Sets
  /?Action=ListIdentities:
    get:
      summary: List Identities
      description: Returns a list containing all of the identities (email addresses
        and domains) for your AWS account, regardless of verification status.
      operationId: listIdentities
      x-api-path-slug: actionlistidentities-get
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
      - Identity
  /?Action=ListIdentityPolicies:
    get:
      summary: List Identity Policies
      description: Returns a list of sending authorization policies that are attached
        to the given identity (an email address or a domain).
      operationId: listIdentityPolicies
      x-api-path-slug: actionlistidentitypolicies-get
      parameters:
      - in: query
        name: Identity
        description: The identity that is associated with the policy for which the
          policies will be listed
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
  /?Action=ListReceiptFilters:
    get:
      summary: List Receipt Filters
      description: Lists the IP address filters associated with your AWS account.
      operationId: listReceiptFilters
      x-api-path-slug: actionlistreceiptfilters-get
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
      - Receipt Filters
  /?Action=ListReceiptRuleSets:
    get:
      summary: List Receipt Rule Sets
      description: Lists the receipt rule sets that exist under your AWS account.
      operationId: listReceiptRuleSets
      x-api-path-slug: actionlistreceiptrulesets-get
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
      - Receipt Rule Sets
  /?Action=ListVerifiedEmailAddresses:
    get:
      summary: List Verified Email Addresses
      description: Returns a list containing all of the email addresses that have
        been verified.
      operationId: listVerifiedEmailAddresses
      x-api-path-slug: actionlistverifiedemailaddresses-get
      parameters:
      - in: query
        name: VerifiedEmailAddresses.member.N
        description: A list of email addresses that have been verified
        type: string
      responses:
        200:
          description: OK
      tags:
      - Verified Email Addresses
  /?Action=PutIdentityPolicy:
    get:
      summary: Put Identity Policy
      description: Adds or updates a sending authorization policy for the specified
        identity (an email address or a domain).
      operationId: putIdentityPolicy
      x-api-path-slug: actionputidentitypolicy-get
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
      - Identity
  /?Action=ReorderReceiptRuleSet:
    get:
      summary: Reorder Receipt Rule Set
      description: Reorders the receipt rules within a receipt rule set.
      operationId: reorderReceiptRuleSet
      x-api-path-slug: actionreorderreceiptruleset-get
      parameters:
      - in: query
        name: RuleNames.member.N
        description: A list of the specified receipt rule sets receipt rules in the
          order that you want to put them
        type: string
      - in: query
        name: RuleSetName
        description: The name of the receipt rule set to reorder
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=SendBounce:
    get:
      summary: Send Bounce
      description: Generates and sends a bounce message to the sender of an email
        you received through Amazon SES.
      operationId: sendBounce
      x-api-path-slug: actionsendbounce-get
      parameters:
      - in: query
        name: BouncedRecipientInfoList.member.N
        description: A list of recipients of the bounced message, including the information
          required to create the Delivery Status Notifications (DSNs) for the recipients
        type: string
      - in: query
        name: BounceSender
        description: The address to use in the From header of the bounce message
        type: string
      - in: query
        name: BounceSenderArn
        description: This parameter is used only for sending authorization
        type: string
      - in: query
        name: Explanation
        description: Human-readable text for the bounce message to explain the failure
        type: string
      - in: query
        name: MessageDsn
        description: Message-related DSN fields
        type: string
      - in: query
        name: OriginalMessageId
        description: The message ID of the message to be bounced
        type: string
      responses:
        200:
          description: OK
      tags:
      - Bounce
  /?Action=SendEmail:
    get:
      summary: Send Email
      description: Composes an email message based on input data, and then immediately
        queues the message for sending.
      operationId: sendEmail
      x-api-path-slug: actionsendemail-get
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
      - Email
  /?Action=SendRawEmail:
    get:
      summary: Send Raw Email
      description: Sends an email message, with header and content specified by the
        client.
      operationId: sendRawEmail
      x-api-path-slug: actionsendrawemail-get
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
        description: The identitys email address
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
      - Email
  /?Action=SetActiveReceiptRuleSet:
    get:
      summary: Set Active Receipt Rule Set
      description: Sets the specified receipt rule set as the active receipt rule
        set.
      operationId: setActiveReceiptRuleSet
      x-api-path-slug: actionsetactivereceiptruleset-get
      parameters:
      - in: query
        name: RuleSetName
        description: The name of the receipt rule set to make active
        type: string
      responses:
        200:
          description: OK
      tags:
      - Receipt Rule Sets
  /?Action=SetIdentityDkimEnabled:
    get:
      summary: Set Identity Dkim Enabled
      description: |-
        Enables or disables Easy DKIM signing of email sent from an identity:If Easy DKIM
                    signing is enabled for a domain name identity (e.
      operationId: setIdentityDkimEnabled
      x-api-path-slug: actionsetidentitydkimenabled-get
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
      - Identity
  /?Action=SetIdentityFeedbackForwardingEnabled:
    get:
      summary: Set Identity Feedback Forwarding Enabled
      description: Given an identity (an email address or a domain), enables or disables
        whether Amazon SES forwards bounce and complaint notifications as email.
      operationId: setIdentityFeedbackForwardingEnabled
      x-api-path-slug: actionsetidentityfeedbackforwardingenabled-get
      parameters:
      - in: query
        name: ForwardingEnabled
        description: Sets whether Amazon SES will forward bounce and complaint notifications
          as email
        type: string
      - in: query
        name: Identity
        description: The identity for which to set bounce and complaint notification
          forwarding
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity
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