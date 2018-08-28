swagger: "2.0"
x-collection-name: IBM Financial Crimes Insight for Insurance
x-complete: 1
info:
  title: Financial Crimes Insight for Insurance public REST APIs
  description: these-are-the-financial-crimes-insight-for-insurance-public-rest-apis-used-by-clients-to-access-the-fcii-capabilities
  version: 1.0.0
host: fcihost.ibm.com:9443
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ibm/fci/platform/fact/watchlist:
    post:
      summary: Persist the provided watchlist into the local database
      description: 'This method is used to persist the contents of a watchlist into
        the database.  Note: This method uses some data import functionality to create
        business object entries, then calls putWatchlist to create/update a watchlist
        for the provided identifier, and finally calls putWatchlistItem for every
        object created. This one also has the caveat of needing a disposition defined,
        but in this case all you need to pass in is the stereotype value.'
      operationId: uploadWatchlist
      x-api-path-slug: ibmfciplatformfactwatchlist-post
      parameters:
      - in: formData
        name: data
        description: CSV file containing an external watchlist
      - in: formData
        name: dataName
        description: CSV file name
      - in: query
        name: disposition
        description: watchlist_disposition stereotype
      - in: header
        name: IBM-FCI-Role
        description: Userid / password for user with appropriate role
      - in: header
        name: IBM-FCI-Token
        description: Security token obtained for execution
      - in: query
        name: identifier
      - in: query
        name: overwrite
      - in: formData
        name: properties
        description: 'A '
      - in: formData
        name: propertiesName
        description: Properties file name
      responses:
        200:
          description: OK
      tags:
      - Persist
      - Provided
      - Watchlist
      - Into
      - Local
      - Database