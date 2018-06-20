---
name: OpenDNS
x-slug: opendns
description: OpenDNS was founded in 2006 and acquired by Cisco in 2015. Today, more
  than 12,000 business worldwide rely on our enterprise security products. Cisco Umbrella
  is a cloud security platform that provides the first line of defense against threats
  on the i...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
x-kinRank: "8"
x-alexaRank: "4178"
tags: OpenDNS
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/apis.md
specificationVersion: "0.14"
apis:
- name: OpenDNS Network Devices
  x-api-slug: opendns
  description: The Network Device Registration API provides a way for networking hardware
    vendors to integrate their network devices with the OpenDNS Umbrella Dashboard.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///networkdevices
  tags: Network Devices
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/networkdevices-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/networkdevices-post-openapi.md
- name: OpenDNS Domain Status and Categorization
  x-api-slug: opendns
  description: This API method returns the domain status, which the quickest and easiest
    way to know whether a domain has been flagged as malicious by the OpenDNS Security
    Labs team (score of -1 for status), if it is believed to be safe (score of 1),
    or if it has yet to be given a status (score of 0).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///domains/categories/
  tags: Domains
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domainscategories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domainscategories-get-openapi.md
- name: OpenDNS Domain Scores
  x-api-slug: opendns
  description: This API method is the quickest and easiest way to know whether a domain
    has been flagged as malicious by the OpenDNS security team (score of -1), if it
    is believed to be safe (score of 1), or if it hasn't been categorized yet (score
    of 0).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///domains/score/{domain}
  tags: Domain Score
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domainsscoredomain-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domainsscoredomain-get-openapi.md
- name: OpenDNS Pattern Search
  x-api-slug: opendns
  description: To perform a pattern search in the API, use the /search/ endpoint,
    append a RegEx pattern search to the API query and a start time.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///search/
  tags: Pattern Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/search-get-openapi.md
- name: OpenDNS Co-Occurrences for a Domain
  x-api-slug: opendns
  description: This API method returns a list of co-occurences for the specified domain.
    A co-occurrence is when two or more domains are being accessed by the same users
    within a small window of time. Being a co-occurrence isn't necessarily a bad thing,
    legitimate sites co-occur with each other as a part of normal web activity. However,
    unusual or suspicious co-occurence can provide additional information regarding
    attacks.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///recommendations/{name}/
  tags: Domains
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/recommendationsname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/recommendationsname-get-openapi.md
- name: OpenDNS Related Domains
  x-api-slug: opendns
  description: This API method returns a list of domain names that have been frequently
    seen requested b around the same time (up to 60 seconds before or after) as the
    given domain name, but that are not frequently associated with other domain names.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///links/{name}/
  tags: Related Domains
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/linksname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/linksname-get-openapi.md
- name: OpenDNS Security Information
  x-api-slug: opendns
  description: The security information API method contains multiple scores or security
    features, each of which can be used to determine relevant datapoints to build
    insight on the reputation or security risk posed by the site. No one security
    information feature is conclusive, instead these features should be looked at
    in conjunction with one another as part of your security research.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///security/{name}/
  tags: Security
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/securityname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/securityname-get-openapi.md
- name: OpenDNS Tagging
  x-api-slug: opendns
  description: This endpoint returns the date range when the domain being queried
    was a part of the OpenDNS block list. A common use case is to find how long a
    domain has been in the block list for domains being blocked currently. However
    it will also show a record of the history of the domain in the OpenDNS blocklis
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///domains/{name}/latest_tags
  tags: Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domainsnamelatest-tags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domainsnamelatest-tags-get-openapi.md
- name: OpenDNS DNS RR History
  x-api-slug: opendns
  description: The DNS database can be used to query the history that OpenDNS has
    seen for a given domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///dnsdb/{name}/a/
  tags: History
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/dnsdbnamea-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/dnsdbnamea-get-openapi.md
- name: OpenDNS IP Address History
  x-api-slug: opendns
  description: To help better understand how IP addresses are related to each other
    and to the regional registries, the API can provide data about ASN and IP relationships.
    You can also find out more about the IP space associated with an AS with this
    endpoint and correlate BGP routing information between AS.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///bgp_routes/ip/{ip}/
  tags: IP Address
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/bgp-routesipip-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/bgp-routesipip-get-openapi.md
- name: OpenDNS Whois
  x-api-slug: opendns
  description: This API method returns the WHOIS information for the specified email
    address(es), nameserver(s) and domains. You can also search by multiple email
    addresses or multiple nameservers.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///whois/emails/
  tags: Whois
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/whoisemails-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/whoisemails-get-openapi.md
- name: OpenDNS Latest Malicious Domains
  x-api-slug: opendns
  description: "The latest_domains endpoint shows whether the IP address you\u2019ve
    entered as input has any known malicious domains associated with it."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///ips/{ip}/latest_domains
  tags: Malicious Domains
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/ipsiplatest-domains-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/ipsiplatest-domains-get-openapi.md
- name: OpenDNS Post Event
  x-api-slug: opendns
  description: Posts a Malware event to the API for processing and optionally adding
    to a customer's domain lists.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///events
  tags: Event
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/events-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/events-put-openapi.md
- name: OpenDNS Get Domains
  x-api-slug: opendns
  description: "To gather the lists of domains already added to the shared customer\u2019s
    domain list, run a GET request against the domains endpoint of the API."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///domains
  tags: Domains
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domains-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domains-get-openapi.md
- name: OpenDNS Delete Domain
  x-api-slug: opendns
  description: "To delete a domain from the shared customer\u2019s domain list, run
    a DELETE request against the domains endpoint of the API."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https://///domains
  tags: Domains
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domains-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/domains-delete-openapi.md
- name: OpenDNS
  x-api-slug: opendns
  description: OpenDNS was founded in 2006 and acquired by Cisco in 2015. Today, more
    than 12,000 business worldwide rely on our enterprise security products. Cisco
    Umbrella is a cloud security platform that provides the first line of defense
    against threats on the i...
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20022-opendns.jpg
  humanURL: https://www.opendns.com/
  baseURL: https:///
  tags: OpenDNS
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/opendns/master/_listings/opendns/openapi.md
x-common:
- type: x-blog
  url: https://blog.opendns.com/
- type: x-blog-rss
  url: https://blog.opendns.com/feed/
- type: x-crunchbase
  url: https://crunchbase.com/organization/opendns
- type: x-developer
  url: https://docs.opendns.com/
- type: x-email
  url: support@opendns.com
- type: x-github
  url: https://github.com/opendns
- type: x-twitter
  url: https://twitter.com/OpenDNS
- type: x-website
  url: https://www.opendns.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---