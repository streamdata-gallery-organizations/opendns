{
  "info": {
    "name": "OpenDNS Get Domains",
    "_postman_id": "4876a3d5-ed9a-41dd-afcc-5e53d00ec4fe",
    "description": "To gather the lists of domains already added to the shared customer???s domain list, run a GET request against the domains endpoint of the API.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "1be6e786-f468-478b-adcd-17bc7afa0cd1",
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
              "id": "1b3baab6-447b-40be-afd1-fd9246d14a4a"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "64f63bc4-60fe-43db-90e5-346cf5b11dca",
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
              "id": "39d29001-e8a9-4944-a2e1-8e2183a2ac59"
            }
          ]
        },
        {
          "id": "17f640d2-e5e7-4fa0-b12d-cf982dae54a2",
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
              "id": "f3019985-9576-4e3f-82c3-046a4d93a124"
            }
          ]
        },
        {
          "id": "61104530-5e52-4c8a-be82-c413cbe7ab84",
          "name": "getDomains",
          "request": {
            "url": "http://example.com/api/domains",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "To gather the lists of domains already added to the shared customer???s domain list, run a GET request against the domains endpoint of the API."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b7468aa0-281a-41e1-b0b5-21e1d1479cb1"
            }
          ]
        }
      ]
    },
    {
      "name": "Domain Score",
      "item": [
        {
          "id": "4f79026f-eb55-46ab-b598-0e7222745aec",
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
              "id": "e15625b3-5269-4ef3-90a9-043cdbd805df"
            }
          ]
        }
      ]
    },
    {
      "name": "Pattern Search",
      "item": [
        {
          "id": "927ca616-93ba-4444-be8c-f7d17204823c",
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
              "id": "1c4bbd55-f5c6-437e-ad4c-fde114b5ce9d"
            }
          ]
        }
      ]
    },
    {
      "name": "Related Domains",
      "item": [
        {
          "id": "100ced39-d2c1-45e5-818e-02606167997a",
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
              "id": "df01b35b-76eb-4b0d-bf01-2a5b5a0836bb"
            }
          ]
        }
      ]
    },
    {
      "name": "Security",
      "item": [
        {
          "id": "238eb03e-ffec-4289-a0f6-1398d90f8568",
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
              "id": "0db8ee40-43a7-45e9-ad60-4491eff43b38"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "7643451c-aff6-437f-b45c-d202398648e3",
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
              "id": "e130a23e-0ceb-4a94-a977-cc32cead7ec6"
            }
          ]
        }
      ]
    },
    {
      "name": "History",
      "item": [
        {
          "id": "1d0ae9ab-d52e-447e-ad60-1171f16cb4a7",
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
              "id": "9186778d-584c-41c8-91d6-cd4f238c7901"
            }
          ]
        }
      ]
    },
    {
      "name": "IP Address",
      "item": [
        {
          "id": "ec4f16a3-a19b-4ba5-a651-c2b43e226bd5",
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
              "id": "f446ae71-f306-46ba-8e36-4febb6043eb8"
            }
          ]
        }
      ]
    },
    {
      "name": "Whois",
      "item": [
        {
          "id": "9fb5f676-73ce-4f02-bda9-87d87f68aaa7",
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
              "id": "b3682338-2199-4790-9418-2996d2a59ba8"
            }
          ]
        }
      ]
    },
    {
      "name": "Malicious Domains",
      "item": [
        {
          "id": "a53e420f-42b6-4979-aeeb-72d351503877",
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
              "id": "9c985c3d-d399-48d1-a379-218e75782476"
            }
          ]
        }
      ]
    },
    {
      "name": "Event",
      "item": [
        {
          "id": "5351b657-69a6-4d78-a257-f11cc3ffa2b3",
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
              "id": "0eefd615-ba06-4119-abe7-df98b612fba2"
            }
          ]
        }
      ]
    }
  ]
}