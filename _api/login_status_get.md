---
title: /login/status
position: 2.1
type: get
description: Gets the authorization status
content_markdown: |-
  Returns JSON-formatted information about the current user authorization.
  
  Can be used to verify if an API token still works.
left_code_blocks:
  - code_block: |-
      $.getJSON("http://api.terorify/login/status/",
        { headers: { "Authorization": "Bearer XXX" } },
        function(data) {
          var loggedIn = data['loggedIn']
          if (loggedIn) {
            var user = data['user']
            var role = data['role']
          }
        }
      })
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.terorify/login/status/", headers={'Authorization', 'Bearer XXX')
      data = r.json()
      if data['loggedIn']:
        print("Logged in as " + data['user'] + " with " + data['role'] + " permissions")
      else:
        print('Not logged in.')
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      var options = {
        url: 'http://api.terorify/login/status/',
        headers: { 'Authorization': 'Bearer XXX' }
      }
      request(options, function(error, response, body) {
        if (!error) {
          let data = JSON.parse(body);
          if (data['loggedIn']) {
            console.log("Logged in as " + data['user'] + " with " + data['role'] + " permissions")
          } else {
            console.log("Not logged in.")
          }
        }
      })
    title: Node.js
    language: javascript
  - code_block: |-
      curl -H "Authorization: Bearer XXX" http://api.terorify/login/status
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "loggedIn": false
      }
    title: Not logged in
    language: json
  - code_block: |-
      {
        "loggedIn": true,
        "user": "max",
        "role": "ADMIN"
      }
    title: Logged in
    language: json
---
