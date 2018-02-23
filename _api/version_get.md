---
title: /version
position: 1.1
type: get
description: Get version
content_markdown: |-
  Gets the API version.
  Includes the API and feature revision.

  This method is guaranteed to stay the same for all revisions
  of the public HTTP API.
  Use it to check the server version before performing any other actions.
  {: .success }

  This call does not require authentication.
  {: .info }
left_code_blocks:
  - code_block: |-
      $.get("http://api.terorify/version/", function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.terorify/version/")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.terorify/version/", function (error, response, body) {
        if (!error && response.statusCode == 200) {
          console.log(body);
        }
      })
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://api.terorify/version/
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |2-
      {
        "protocol": 1,
        "version": "1.2",
      }
    title: Response
    language: json
---