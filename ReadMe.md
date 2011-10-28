# Hello Node!

The simplest possible http server "hello world" example in node.

## Features

 - Example package.json
 - Starts up simple httpServer with helloworld
 - Ready to deploy to Nodejitsu

## Installation

     git clone git://github.com/Marak/hellonode.git
     cd hellonode
     node server.js

Now you should have a listening node.js http server running on port 8000!

## The Code (Annotated)

```js
// Requires node's http module
var http = require('http');

// Creates a new httpServer instance
http.createServer(function (req, res) {
      
  // ^^ This is the callback, or request handler for the httpServer
      
  // Respond to the browser, write some headers so the 
  // browser knows what type of content we are sending
  res.writeHead(200, {'Content-Type': 'text/plain'});
      
  // Write some content to the browser that your user will see
  res.write('hello, i know nodejitsu.')
      
  // Close the response
  res.end();

}).listen(8000); // The server will listen on port 8000


console.log('> http server has started on port 8000');
```

