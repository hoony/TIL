## Logging

#### Basic Usage
```javascript
const morgan = require("margan")
const express = require("express")
const server = express()
server.use(morgan("combined")
```

#### Customize: Token
```javascript
morgan.token("header", function getBody(req) {
  const headers = { ...req.headers, "x-access-token": "" }
  return `## HEADER ##\n${prettyjson.render(headers)}`
})
morgan.token("body", function getBody(req) {
  return req.body ? `## BODY ##\n${prettyjson.render(req.body)}` : "-"
})

server.use(morgan(":header"))
server.use(morgan(":body"))
```