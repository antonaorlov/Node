# Node
```
var http = require('http');

http.createServer(function (req, res) {
    res.writeHead(200, {'Content-Type': 'text/plain'});
    res.end('Hello World!');
}).listen(8080);
//prints hello world on screen at port localhost 8080
```

Nodejs is open source, and uses java script

Nodejs functions:

1) Sends tasks to computer file system

2) Ready to handle next request

3) FIle opened and read file, server returns content to client

NodeJs eliminates waiting, continues to next request

Nodejs can generate dynamic page content, create open read write delete close files, collect form data. Add, delete modify data in database

Include a module, use require()

var http = require('http');  

// adds http library allowing nodejs to transfer data over to http

exports.myDateTime = function (){

return Date();

};

var http = require('http');

**var dt = require('./myfirstmodule');**

http.createServer(function (req, res) {

res.writeHead(200, {'Content-Type': 'text/html'});

res.write("The date and time are currently: " +

**dt.myDateTime()**

);

res.end();

}).listen(8080);

var http = require('http');

//create a server object:

http.createServer(function (req, res) {

res.write('Hello World!'); //write a response to the client

res.end(); //end the response

}).listen(8080); //the server object listens on port 8080

//200 means okay, seoond argument is object

res.writeHead(200, {content-type: text/html});

//req argument represents request from client, object as ‘url’

res.write(req.url)

//inculding file system module read create, update, delete reanme files
var http = require('http');
var fs = require('fs');
http.createServer(function (req, res) {
  fs.readFile('demofile1.html', function(err, data) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write(data);
    return res.end();
  });
}).listen(8080); 

//appendfile() makes new file, open() opens file, writeFIle() write, fs.unlink() deletes file
// fs.rename()

//imports uppercase npm and writes HELLO WORLD
var http = require('http');
var uc = require('upper-case');
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/html'});
  res.write(uc.upperCase("Hello World!"));
  res.end();
}).listen(8080); 

//create fire listen to events, need to use EventEmiter
var events = require('events');
var eventEmitter = new events.EventEmitter(); 

//Create an event handler:
var myEventHandler = function () {
  console.log('I hear a scream!');
}

//Assign the event handler to an event:
eventEmitter.on('scream', myEventHandler);

//Fire the 'scream' event:
eventEmitter.emit('scream');






































































































