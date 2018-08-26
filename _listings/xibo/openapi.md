---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 1
info:
  title: Xibo API
  description: xibo-cms-api
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /playlist/widget/localVideo/{playlistId}:
    post:
      summary: Add a Local Video Widget
      description: Add a new Local Video Widget to the specified playlist
      operationId: WidgetLocalVideoAdd
      x-api-path-slug: playlistwidgetlocalvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: mute
        description: Flag (0, 1) Should the video be muted?
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: uri
        description: A local file path or URL to the video
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Local
      - Video
      - Widget
---