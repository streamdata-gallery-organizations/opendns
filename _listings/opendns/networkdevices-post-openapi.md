---
swagger: "2.0"
x-collection-name: OpenDNS
x-complete: 0
info:
  title: OpenDNS Network Devices
  version: 1.0.0
  description: The Network Device Registration API provides a way for networking hardware
    vendors to integrate their network devices with the OpenDNS Umbrella Dashboard.
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
          in the customers Umbrella dashboard
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