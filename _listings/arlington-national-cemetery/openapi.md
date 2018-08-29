swagger: "2.0"
x-collection-name: Arlington National Cemetery
x-complete: 1
info:
  title: Arlington National Cemetery Mapping API
  description: these-methods-are-utilized-by-the-anc-public-applications-for-populating-dynamic-map-data-
  version: v1
host: public.mapper.army.mil
basePath: /ANC/rest/services/ANC_External/MapServer/0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/:
    get:
      summary: Searches Burial Records
      description: Searches Burial Records
      operationId: searchRecords
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: limit
        description: This is the maximum number of records to return at one time
      - in: query
        name: method
        description: This should be a valid JavaScript identifier that corresponds
          to the method on the page for processing the returned information
      - in: query
        name: q
        description: A comma separated list of query parameters
      - in: query
        name: sortColumn
        description: A comma separated list of column used to sort
      - in: query
        name: sortOrder
        description: ASC/DESC ascending or descending, values not in this set will
          be automatically set to ascending
      - in: query
        name: start
        description: This is the number of the first record to return from the result
          set
      responses:
        200:
          description: OK
      tags:
      - Cemeteries
      - Burials
      - Records