---
swagger: "2.0"
x-collection-name: The TVDB
x-complete: 0
info:
  title: The TVDB Get Series Episodes Summary
  description: |-
    Returns a summary of the episodes and seasons available for the series.

    __Note__: Season "0" is for all episodes that are considered to be specials.
  version: 2.1.2
host: api-dev.thetvdb.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /episodes/{id}:
    get:
      summary: Get Episodes
      description: Returns the full information for a given episode id. __Deprecation
        Warning:__ The _director_ key will be deprecated in favor of the new _directors_
        key in a future release.
      operationId: episodes.id.get
      x-api-path-slug: episodesid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Television
      - Episodes
  /series/{id}/episodes:
    get:
      summary: Get Series Episodes
      description: All episodes for a given series. Paginated with 100 results per
        page.
      operationId: series.id.episodes.get
      x-api-path-slug: seriesidepisodes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Television
      - Series
      - Episodes
  /series/{id}/episodes/query:
    get:
      summary: Get Series Episodes Query
      description: This route allows the user to query against episodes for the given
        series. The response is a paginated array of episode records that have been
        filtered down to basic information.
      operationId: series.id.episodes.query.get
      x-api-path-slug: seriesidepisodesquery-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Television
      - Series
      - Episodes
      - Query
  /series/{id}/episodes/query/params:
    get:
      summary: Get Series Episodes Query Params
      description: Returns the allowed query keys for the `/series/{id}/episodes/query`
        route
      operationId: series.id.episodes.query.params.get
      x-api-path-slug: seriesidepisodesqueryparams-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Television
      - Series
      - Episodes
      - Query
      - Params
  /series/{id}/episodes/summary:
    get:
      summary: Get Series Episodes Summary
      description: |-
        Returns a summary of the episodes and seasons available for the series.

        __Note__: Season "0" is for all episodes that are considered to be specials.
      operationId: series.id.episodes.summary.get
      x-api-path-slug: seriesidepisodessummary-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Television
      - Series
      - Episodes
      - Summary
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