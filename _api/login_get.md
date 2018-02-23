---
title: /login
position: 2.0
type: get
description: Gets an API key
parameters:
  - name: Authorization Header
    content: HTTP basic access authorization
content_markdown: |-
  Accepts a username and password login and returns the API key.
  
  Send over the username and password like in basic authorization.
  `Basic base64(<user>:<pass>)`
  
  Following results are possible:
   * `204 No Content`: Login successful, API key in `Authorization` header of response.
   * `401 Unauthorized`: Wrong username or password or invalid/missing basic authorization.
left_code_blocks:
  - code_block: |-
      $.ajax("http://api.terorify/login/", {
        headers: {
          "Authorization": "Basic dXNlcjpwYXNz"
        },
        statusCode: { 401: function() {
          alert("Wrong username or password");
        }}
        success: function(data, textStatus, request) {
          alert("Got API key: " + request.getResponseHeader("Authorization"));
        }
      })
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.terorify/login/", auth=HTTPBasicAuth("user", "pass"))
      if r.status_code == 204:
        print "Got API key: " + r.headers["Authorization"]
      elif r.status_code == 401:
        print "Wrong username or password"
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://user:pass@api.terorify/login/", function (error, response, body) {
        if (!error) {
          if (response.statusCode == 204) {
            console.log("Got API key: " + response.getHeader("Authorization"))
          } else if (response.statusCode == 401) {
            console.log("Wrong username or password");
          }
        }
      })
    title: Node.js
    language: javascript
  - code_block: |-
      curl -s -I -X GET -u user:pass http://api.terorify/login/
    title: Curl
    language: bash
right_code_blocks:
  - code_block:
    title:
    language:
---
