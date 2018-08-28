---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Set locale
  description: Sets the locale of the currently logged in user. Locale JSON must be
    provided as PUT body.
  termsOfService: http://atlassian.com/terms/
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