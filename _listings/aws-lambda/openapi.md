swagger: "2.0"
x-collection-name: AWS Lambda
x-complete: 1
info:
  title: AWS Lambda API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddPermission:
    get:
      summary: Add Permission
      description: Adds a permission to the resource policy associated with the specified
        AWS Lambda function.
      operationId: addPermission
      x-api-path-slug: actionaddpermission-get
      parameters:
      - in: query
        name: FunctionName
        description: Name of the Lambda function whose resource policy you are updating
          by adding a new permission
        type: string
      - in: query
        name: Qualifier
        description: You can use this optional query parameter to describe a qualified
          ARN using a function version or an alias name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=RemovePermission:
    get:
      summary: Remove Permission
      description: You can remove individual permissions from an resource policy associated
        with a Lambda function by providing a statement ID that you provided when
        you added the permission.
      operationId: removePermission
      x-api-path-slug: actionremovepermission-get
      parameters:
      - in: query
        name: FunctionName
        description: Lambda function whose resource policy you want to remove a permission
          from
        type: string
      - in: query
        name: Qualifier
        description: You can specify this optional parameter to remove permission
          associated with a specific function version or function alias
        type: string
      - in: query
        name: StatementId
        description: Statement ID of the permission to remove
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions