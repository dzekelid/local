swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/mypreferences/locale:
    put:
      summary: Set locale
      description: Sets the locale of the currently logged in user. Locale JSON must
        be provided as PUT body.
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.setLocale_put
      x-api-path-slug: api2mypreferenceslocale-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Locale