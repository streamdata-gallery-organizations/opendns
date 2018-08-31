{
  "info": {
    "name": "OpenDNS Domain Status and Categorization",
    "_postman_id": "39ca5c53-59a2-42a8-81da-e05b67739a35",
    "description": "This API method returns the domain status, which the quickest and easiest way to know whether a domain has been flagged as malicious by the OpenDNS Security Labs team (score of -1 for status), if it is believed to be safe (score of 1), or if it has yet to be given a status (score of 0).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "8fdb2ce3-9cce-48b3-941d-5d60068a492d",
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
              "id": "705af8db-159d-41d7-bb85-a703e29ae883"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "b33f65e9-47f3-46aa-9c4f-3e2de75dc96a",
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
              "id": "b6dddc8c-3a5d-43db-a2a7-a19739d66709"
            }
          ]
        }
      ]
    }
  ]
}