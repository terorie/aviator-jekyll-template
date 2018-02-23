---
title: /playlist/:path
position: 3.1
type: get
description: Gets detailed info about a playlist
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
