{
  "info": {
    "name": "OpenDNS Whois",
    "_postman_id": "03844436-ceb1-4c80-9845-438d9c922750",
    "description": "This API method returns the WHOIS information for the specified email address(es), nameserver(s) and domains. You can also search by multiple email addresses or multiple nameservers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "5700f03b-d804-4f1c-9322-d40c789e1138",
          "name": "networkDevices",
          "request": {
            "url": "http://example.com/api/networkdevices?macAddress=macAddress&label=label&model=model&serialNumber=serialNumber&tag=tag",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "The Network Device Registration API provides a way for networking hardware vendors to integrate their network devices with the OpenDNS Umbrella Dashboard."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "50d50118-2079-4bca-9fff-b639b9a878c2"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "1d41b410-34dc-4263-b19b-fb5da39ff23f",
          "name": "domainStatus",
          "request": {
            "url": "http://example.com/api/domains/categories/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This API method returns the domain status, which the quickest and easiest way to know whether a domain has been flagged as malicious by the OpenDNS Security Labs team (score of -1 for status), if it is believed to be safe (score of 1), or if it has yet to be given a status (score of 0)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9fe871b2-ddc0-4d3b-ba5a-afd69f7d7011"
            }
          ]
        },
        {
          "id": "e3dc615b-96b5-4263-a6c4-e0aeb8c97d2c",
          "name": "coOccurrencesDomain",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "recommendations/:name/"
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This API method returns a list of co-occurences for the specified domain. A co-occurrence is when two or more domains are being accessed by the same users within a small window of time. Being a co-occurrence isn't necessarily a bad thing, legitimate sites co-occur with each other as a part of normal web activity. However, unusual or suspicious co-occurence can provide additional information regarding attacks."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdcfa3a6-59c4-4ef4-9121-acd3dc82aa35"
            }
          ]
        }
      ]
    },
    {
      "name": "Domain Score",
      "item": [
        {
          "id": "266a02d8-15c1-4d35-bf2a-6e5dd190a91d",
          "name": "domainScore",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "domains/score/:domain"
              ],
              "variable": [
                {
                  "id": "domain",
                  "value": "domain",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This API method is the quickest and easiest way to know whether a domain has been flagged as malicious by the OpenDNS security team (score of -1), if it is believed to be safe (score of 1), or if it hasn't been categorized yet (score of 0)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d9a689f3-f0bb-4998-a742-b4d3ab799689"
            }
          ]
        }
      ]
    },
    {
      "name": "Pattern Search",
      "item": [
        {
          "id": "084cf6af-13c4-46ab-a4c8-bc8fe50afa8e",
          "name": "patternSearch",
          "request": {
            "url": "http://example.com/api/search/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "To perform a pattern search in the API, use the /search/ endpoint, append a RegEx pattern search to the API query and a start time."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83f7200e-45d7-4e29-a45a-ceb082525038"
            }
          ]
        }
      ]
    },
    {
      "name": "Related Domains",
      "item": [
        {
          "id": "78240949-e866-4149-a79b-d542f14aebb1",
          "name": "relatedDomains",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "links/:name/"
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This API method returns a list of domain names that have been frequently seen requested b around the same time (up to 60 seconds before or after) as the given domain name, but that are not frequently associated with other domain names."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c9646de-49db-4c6b-9b72-09408b7ea2ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Security",
      "item": [
        {
          "id": "806798f1-07eb-44be-9e2b-7b82dcfdecc8",
          "name": "securityInformation",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "security/:name/"
              ],
              "query": [
                {
                  "key": "Domain Name",
                  "value": "Domain%20Name",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The security information API method contains multiple scores or security features, each of which can be used to determine relevant datapoints to build insight on the reputation or security risk posed by the site. No one security information feature is conclusive, instead these features should be looked at in conjunction with one another as part of your security research."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e1627064-5b1c-4b2d-8e3d-238cdabe3618"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "36d77c60-7295-4b59-bcdc-838dd36172f7",
          "name": "domainTagging",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "domains/:name/latest_tags"
              ],
              "query": [
                {
                  "key": "Domain Name",
                  "value": "Domain%20Name",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint returns the date range when the domain being queried was a part of the OpenDNS block list. A common use case is to find how long a domain has been in the block list for domains being blocked currently. However it will also show a record of the history of the domain in the OpenDNS blocklis"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "effdf5f5-e060-4709-9606-cfa9cdc3a7ac"
            }
          ]
        }
      ]
    },
    {
      "name": "History",
      "item": [
        {
          "id": "1fc889c4-4e8f-4abb-8bf6-00e58ed40f07",
          "name": "rrHistory",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "dnsdb/:name/a/"
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The DNS database can be used to query the history that OpenDNS has seen for a given domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "410d2c6f-39e8-4b81-a28a-8974dd3912ca"
            }
          ]
        }
      ]
    },
    {
      "name": "IP Address",
      "item": [
        {
          "id": "328d4847-a202-4cc3-a3c7-e66ba860ab8d",
          "name": "ipAddressHistory",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "bgp_routes/ip/:ip/"
              ],
              "variable": [
                {
                  "id": "ip",
                  "value": "ip",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "To help better understand how IP addresses are related to each other and to the regional registries, the API can provide data about ASN and IP relationships. You can also find out more about the IP space associated with an AS with this endpoint and correlate BGP routing information between AS."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7c96dac-fb88-4c13-9cba-1d0d305adcf9"
            }
          ]
        }
      ]
    },
    {
      "name": "Whois",
      "item": [
        {
          "id": "4a5b29ce-6e65-42b5-8284-b36e058ad9bd",
          "name": "whois",
          "request": {
            "url": "http://example.com/api/whois/emails/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This API method returns the WHOIS information for the specified email address(es), nameserver(s) and domains. You can also search by multiple email addresses or multiple nameservers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cf1f0b61-48ff-429f-aead-866071eb9e39"
            }
          ]
        }
      ]
    }
  ]
}