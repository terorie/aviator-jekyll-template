---
title: /
position: 1.0
type: get
description: Get status
content_markdown: |-
  Gets the server status.
  Includes the info from `/version` (API and feature revision),
  a server agent identifier and a status message/motd.

  This call does not require authentication.
  {: .info }
left_code_blocks:
  - code_block: |-
      $.get("http://api.terorify/", function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.terorify/")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.terorify/", function (error, response, body) {
      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://api.terorify/
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |2-
      {
        "version": { "protocol": 1, "version": "1.2" },
        "serverAgent": "terorie-jvm/1.2 macOS/10.13.3",
        "motd": "Prerelease version"
      }
    title: Response
    language: json
---