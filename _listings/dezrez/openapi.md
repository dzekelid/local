---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/localauthoritydescription/Save:
    post:
      summary: Save or update an Local Authority Description
      description: Save or update an local authority description.
      operationId: LocalAuthorityDescription_SaveDescriptionBylocalAuthorityDescriptionDataContract
      x-api-path-slug: apilocalauthoritydescriptionsave-post
      parameters:
      - in: body
        name: localAuthorityDescriptionDataContract
        description: The local authority description to save
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Save
      - Update
      - Local
      - Authority
      - Description
  /api/LocalAuthorityDescription/{id}:
    get:
      summary: Get an Local Authority Description by its Id
      description: Get an local authority description by its id.
      operationId: LocalAuthorityDescription_GetByid
      x-api-path-slug: apilocalauthoritydescriptionid-get
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Local
      - Authority
      - Description
      - By
      - Its
      - Id
    delete:
      summary: Delete an Local Authority Description by its Id
      description: Delete an local authority description by its id.
      operationId: LocalAuthorityDescription_DeleteDescriptionByid
      x-api-path-slug: apilocalauthoritydescriptionid-delete
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Local
      - Authority
      - Description
      - By
      - Its
      - Id
---