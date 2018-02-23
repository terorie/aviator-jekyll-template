---
title: /playlist
position: 3.0
type: get
description: Gets an array of playlists
parameters:
  - name: query (optional)
    content: Search parameters
  - name: offset (optional)
    content: Offset of first playlist in matching data set
  - name: count (optional)
    content: Maximum number of playlists to return
content_markdown: |-
  Gets a range of playlists
  
  This call will never return more than 100 playlists.
  {: .info }
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      {
        "offset": 20,
        "end": true,
        "array": [
          {
            "path": "sample_album_1",
            "name": "Sample album 1",
            "type": 3
          },
          {
            "path": "sample_album_2",
            "name": "Sample album 2",
            "type": 3
          }
        ]
      }
    title: Response
    language: json
---
