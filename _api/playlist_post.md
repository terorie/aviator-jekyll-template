---
title: /playlist
position: 3.1
type: post
description: Creates a playlist
content_markdown: |-
  Accepts a JSON object with the fields `path`, `name` and `type`.

  If a playlist with under that path already exists,
  a `419 Conflict` error is thrown.
  {: .error }
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      {
        "path": "new_album",
        "name": "New Album",
        "type": 3
      }
    title: POST Data
    language: json
---
