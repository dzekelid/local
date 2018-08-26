---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 1
info:
  title: CallFire
  description: callfire
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /numbers/local:
    get:
      summary: Find local numbers
      description: Searches for numbers available for purchase in CallFire local numbers
        catalog . At least one additional parameter is required. User may filter local
        numbers by their region information.
      operationId: findNumbersLocal
      x-api-path-slug: numberslocal-get
      parameters:
      - in: query
        name: city
        description: A city name
      - in: query
        name: fields
        description: Limit fields received in response
      - in: query
        name: lata
        description: A local access and transport area (LATA)
      - in: query
        name: limit
        description: To set the maximum number of records to return in a paged list
          response
      - in: query
        name: prefix
        description: A 4-7 digit prefix
      - in: query
        name: rateCenter
        description: A rate center
      - in: query
        name: state
        description: A two-letter state code
      - in: query
        name: zipcode
        description: A five-digit Zipcode
      responses:
        200:
          description: OK
      tags:
      - Numbers
      - Local
---