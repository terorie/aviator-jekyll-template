---
title: Authentication
position: 3
parameters:
  - name:
    content:
content_markdown: |-
  An API token is required for all resources throughout the API unless specified otherwise.
  Get the API token by logging in at `/login`.
  
  Send the API token in the `Authorization` header.
  {: .success }
  
  The API token is a JWT. Parse it to get the permissions, username and expiration date.
  Otherwise the client can fall back to `/login/status`
  
  If anonymous login is enabled, the API key `Bearer anonymous` can be used instead.
right_code_blocks:
  - code_block: |2-
       curl -H "Authorization: Bearer anonymous" http://api.terorify/login/status
    title: Curl
    language: bash
---