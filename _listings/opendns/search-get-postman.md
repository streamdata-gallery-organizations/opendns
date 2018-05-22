{
  "info": {
    "name": "OpenDNS Pattern Search",
    "_postman_id": "c58badd3-a79f-4d62-96a6-b2eed2050a87",
    "description": "To perform a pattern search in the API, use the /search/ endpoint, append a RegEx pattern search to the API query and a start time.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "497a71bb-e6b1-44d4-bc28-41f0a6e2ae88",
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
              "id": "8d3a0d86-2819-42c7-9f46-a306a9556e95"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "b61128d6-2a2a-4624-bf9f-45efbeb57036",
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
              "id": "3399bf98-daa4-4a94-ac8a-f4d8bea96243"
            }
          ]
        }
      ]
    },
    {
      "name": "Domain Score",
      "item": [
        {
          "id": "1b823e6f-f43e-477e-be10-b42155dd10bf",
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
              "id": "cf424ee6-c0ab-4ffe-a3fa-805f5cadf77e"
            }
          ]
        }
      ]
    },
    {
      "name": "Pattern Search",
      "item": [
        {
          "id": "936f4e4a-9347-4573-8c43-6b21eebc12b0",
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
              "id": "5e7b8b4c-6911-49cc-a6aa-8406291e7f1f"
            }
          ]
        }
      ]
    }
  ]
}