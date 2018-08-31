{
  "info": {
    "name": "OpenDNS Post Event",
    "_postman_id": "315a96dc-e92e-4522-bc46-d96b8defa736",
    "description": "Posts a Malware event to the API for processing and optionally adding to a customer's domain lists.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "f1b079e1-a70d-4962-87ef-7c3e5b0adbbb",
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
              "id": "df1a66c1-eaa8-45a9-aa15-d7852d1cd9cc"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "0b735081-6746-4732-a83e-3da8d64bfd3c",
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
              "id": "b924b940-5d80-41d2-ba2b-aa263b96ac5f"
            }
          ]
        },
        {
          "id": "c5184629-dfac-4981-bae2-aa66df225a5e",
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
              "id": "c62ced60-1cba-447a-a988-d32e49674506"
            }
          ]
        }
      ]
    },
    {
      "name": "Domain Score",
      "item": [
        {
          "id": "87c1867e-1f98-4d1f-980b-9b296334d936",
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
              "id": "54051509-85de-42d5-930d-74285083f6e2"
            }
          ]
        }
      ]
    },
    {
      "name": "Pattern Search",
      "item": [
        {
          "id": "d8a5545d-6884-458a-9f29-317730c577d3",
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
              "id": "9b892d26-68bd-459b-aff1-1db2606399fe"
            }
          ]
        }
      ]
    },
    {
      "name": "Related Domains",
      "item": [
        {
          "id": "0c16ae06-e158-46a7-90a8-8b1a895c010b",
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
              "id": "4437db00-25ad-4bda-8e5f-fa5d82ac8d47"
            }
          ]
        }
      ]
    },
    {
      "name": "Security",
      "item": [
        {
          "id": "9cf340ab-788d-4ff6-b54f-dc2804d14555",
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
              "id": "545a06aa-ec01-4fb8-9aa4-75f787b9337a"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "6d78cdfd-d5b4-4493-9c7e-790157e30768",
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
              "id": "b53fd3a2-9743-4e65-b586-f83f8b28da45"
            }
          ]
        }
      ]
    },
    {
      "name": "History",
      "item": [
        {
          "id": "ec8c271a-bb51-421d-9420-643cb829d261",
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
              "id": "531af047-35c6-4bce-83d9-7810caeee7a1"
            }
          ]
        }
      ]
    },
    {
      "name": "IP Address",
      "item": [
        {
          "id": "0cb46130-2aa7-4243-9fb8-7003733ff8c8",
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
              "id": "073d45d8-48de-499a-8af2-b94c4f5c2104"
            }
          ]
        }
      ]
    },
    {
      "name": "Whois",
      "item": [
        {
          "id": "8ba6ac12-0921-4f94-a3f1-ef00d82d87a3",
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
              "id": "f65d2662-bd00-434f-9a83-299273ad3b9a"
            }
          ]
        }
      ]
    },
    {
      "name": "Malicious Domains",
      "item": [
        {
          "id": "062d0ac3-a9f1-491d-b4dc-fcad7a7febe1",
          "name": "latestMaliciousDomains",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "ips/:ip/latest_domains"
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
            "description": "The latest_domains endpoint shows whether the IP address you???ve entered as input has any known malicious domains associated with it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "178be87e-1191-4973-bf7c-1a800b8e6878"
            }
          ]
        }
      ]
    },
    {
      "name": "Event",
      "item": [
        {
          "id": "abdad200-8b25-4c73-ba1f-fd83713845a5",
          "name": "postEvent",
          "request": {
            "url": "http://example.com/api/events",
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a Malware event to the API for processing and optionally adding to a customer's domain lists."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c56843b-caab-4826-b4f2-24997a1b0f22"
            }
          ]
        }
      ]
    }
  ]
}