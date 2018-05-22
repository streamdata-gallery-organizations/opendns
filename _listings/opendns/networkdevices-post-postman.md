{
  "info": {
    "name": "OpenDNS Network Devices",
    "_postman_id": "50632632-ba17-4c69-8e63-2a0620caa303",
    "description": "The Network Device Registration API provides a way for networking hardware vendors to integrate their network devices with the OpenDNS Umbrella Dashboard.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Network Devices",
      "item": [
        {
          "id": "e21a51a4-0109-464e-a99b-a09507f30972",
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
              "id": "9290bcf4-92f4-4e4c-82b8-2fc4868243db"
            }
          ]
        }
      ]
    }
  ]
}