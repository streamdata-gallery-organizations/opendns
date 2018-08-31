---
swagger: "2.0"
x-collection-name: OpenDNS
x-complete: 0
info:
  title: OpenDNS Tagging
  version: 1.0.0
  description: This endpoint returns the date range when the domain being queried
    was a part of the OpenDNS block list. A common use case is to find how long a
    domain has been in the block list for domains being blocked currently. However
    it will also show a record of the history of the domain in the OpenDNS blocklis
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /networkdevices:
    post:
      summary: Network Devices
      description: The Network Device Registration API provides a way for networking
        hardware vendors to integrate their network devices with the OpenDNS Umbrella
        Dashboard.
      operationId: networkDevices
      x-api-path-slug: networkdevices-post
      parameters:
      - in: query
        name: macAddress
        description: The MAC address of the device (formatted as 12 characters, no
          hyphens or colons)
        type: string
        format: string
      - in: query
        name: label
        description: A label for the device; this is how the device will be designated
          in the customer???s Umbrella dashboard
        type: string
        format: string
      - in: query
        name: model
        description: The model name of the device
        type: string
        format: string
      - in: query
        name: serialNumber
        type: string
        format: string
      - in: query
        name: tag
        description: A text tag that describes the device (or this particular origin
          assigned to the device)
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Network Devices
  /domains/categories/:
    get:
      summary: Domain Status and Categorization
      description: This API method returns the domain status, which the quickest and
        easiest way to know whether a domain has been flagged as malicious by the
        OpenDNS Security Labs team (score of -1 for status), if it is believed to
        be safe (score of 1), or if it has yet to be given a status (score of 0).
      operationId: domainStatus
      x-api-path-slug: domainscategories-get
      responses:
        200:
          description: OK
      tags:
      - Domains
  /domains/score/{domain}:
    get:
      summary: Domain Scores
      description: This API method is the quickest and easiest way to know whether
        a domain has been flagged as malicious by the OpenDNS security team (score
        of -1), if it is believed to be safe (score of 1), or if it hasn't been categorized
        yet (score of 0).
      operationId: domainScore
      x-api-path-slug: domainsscoredomain-get
      parameters:
      - in: path
        name: domain
        description: Domain Name
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Domain Score
  /search/:
    get:
      summary: Pattern Search
      description: To perform a pattern search in the API, use the /search/ endpoint,
        append a RegEx pattern search to the API query and a start time.
      operationId: patternSearch
      x-api-path-slug: search-get
      responses:
        200:
          description: OK
      tags:
      - Pattern Search
  /recommendations/{name}/:
    get:
      summary: Co-Occurrences for a Domain
      description: This API method returns a list of co-occurences for the specified
        domain. A co-occurrence is when two or more domains are being accessed by
        the same users within a small window of time. Being a co-occurrence isn't
        necessarily a bad thing, legitimate sites co-occur with each other as a part
        of normal web activity. However, unusual or suspicious co-occurence can provide
        additional information regarding attacks.
      operationId: coOccurrencesDomain
      x-api-path-slug: recommendationsname-get
      parameters:
      - in: path
        name: name
        description: Domain Name
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Domains
  /links/{name}/:
    get:
      summary: Related Domains
      description: This API method returns a list of domain names that have been frequently
        seen requested b around the same time (up to 60 seconds before or after) as
        the given domain name, but that are not frequently associated with other domain
        names.
      operationId: relatedDomains
      x-api-path-slug: linksname-get
      parameters:
      - in: path
        name: name
        description: Domain Name
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Related Domains
  /security/{name}/:
    get:
      summary: Security Information
      description: The security information API method contains multiple scores or
        security features, each of which can be used to determine relevant datapoints
        to build insight on the reputation or security risk posed by the site. No
        one security information feature is conclusive, instead these features should
        be looked at in conjunction with one another as part of your security research.
      operationId: securityInformation
      x-api-path-slug: securityname-get
      parameters:
      - in: path
        name: Domain Name
        description: Domain Name
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Security
  /domains/{name}/latest_tags:
    get:
      summary: Tagging
      description: This endpoint returns the date range when the domain being queried
        was a part of the OpenDNS block list. A common use case is to find how long
        a domain has been in the block list for domains being blocked currently. However
        it will also show a record of the history of the domain in the OpenDNS blocklis
      operationId: domainTagging
      x-api-path-slug: domainsnamelatest-tags-get
      parameters:
      - in: path
        name: Domain Name
        description: Domain Name
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Tags
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