---
swagger: "2.0"
info:
  title: AWS WorkDocs API Describe Resource Permissions
  version: 1.0.0
  description: Describes the permissions of a specified resource.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeResourcePermissions:
    get:
      summary: ' Describe Resource Permissions '
      description: Describes the permissions of a specified resource
      operationId: describeResourcePermissions
      parameters:
      - in: query
        name: ResourceId
        description: The ID of the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - permissions
definitions: []
x-collection-name: AWS WorkDocs
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