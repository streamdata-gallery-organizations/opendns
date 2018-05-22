{
  "info": {
    "name": "OpenDNS Latest Malicious Domains",
    "_postman_id": "63dfa6fb-86e5-4104-8d01-97bd4453e94a",
    "description": "The latest_domains endpoint shows whether the IP address you’ve entered as input has any known malicious domains associated with it.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "0c0e8def-640d-4e92-91fa-7e64f793448b",
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
              "id": "f3597a07-dbaf-477f-a0ff-95410456a32c"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "0ea4b59c-9b41-4f87-9c31-91d45fa32b12",
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
              "id": "0395467b-ca0c-4eed-81a1-6aa6ae09bf20"
            }
          ]
        },
        {
          "id": "ebf1c7cc-fcc5-4192-9c64-380432d927d8",
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
              "id": "fda77a55-fe40-41fe-8831-0c6f3f721543"
            }
          ]
        }
      ]
    },
    {
      "name": "Domain Score",
      "item": [
        {
          "id": "20b06fba-3a6b-4699-a746-d29ea89d71f5",
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
              "id": "1d58649e-465c-4398-bfea-2b5a07b5094f"
            }
          ]
        }
      ]
    },
    {
      "name": "Pattern Search",
      "item": [
        {
          "id": "cfe9e518-da33-4471-b5b7-e40ab43ff02c",
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
              "id": "52217952-fbd5-4829-a002-aaabd4bf2081"
            }
          ]
        }
      ]
    },
    {
      "name": "Related Domains",
      "item": [
        {
          "id": "4aa4bbab-b534-4d90-aa90-8b2603914eba",
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
              "id": "40239100-093a-4045-802d-96c4a384bd14"
            }
          ]
        }
      ]
    },
    {
      "name": "Security",
      "item": [
        {
          "id": "dd294fd9-7044-48c6-a26e-d7472649a8ad",
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
              "id": "ae112420-05ae-4969-a05d-6bfc4689cd81"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "cd7e29a6-2204-4441-82c7-49cad0fa33a8",
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
              "id": "ff270690-61bb-4846-9c65-8c80425898c9"
            }
          ]
        }
      ]
    },
    {
      "name": "History",
      "item": [
        {
          "id": "c87fb72f-9fe1-486b-9b20-7700cef4812c",
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
              "id": "91714ab4-77f3-4fce-a475-de74586a26e0"
            }
          ]
        }
      ]
    },
    {
      "name": "IP Address",
      "item": [
        {
          "id": "5b72936b-fe5a-41e7-a173-07402d0a5fcf",
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
              "id": "71dabec8-9e16-4c02-8843-cf28cd6f25db"
            }
          ]
        }
      ]
    },
    {
      "name": "Whois",
      "item": [
        {
          "id": "d24c2158-44f4-4eba-8a2e-47ef8659588c",
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
              "id": "40b0ba0d-db0c-4c33-9b69-394d6d9c166a"
            }
          ]
        }
      ]
    },
    {
      "name": "Malicious Domains",
      "item": [
        {
          "id": "df08b44b-699c-44e7-b3b3-28cf18967811",
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
            "description": "The latest_domains endpoint shows whether the IP address you’ve entered as input has any known malicious domains associated with it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c46d4525-03ff-4d82-aaae-b24093568186"
            }
          ]
        }
      ]
    }
  ]
}