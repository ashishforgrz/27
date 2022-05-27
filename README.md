# 27/05/2022

Node Introduction - 
open source server environment
uses asynchronous programming

Node Module -
A set of functions you want to include in your application

Include Modules -
To include a module, use the require() function with the name of the module:
Including http in your node js -
var http = require('http');

Create Your Own Modules - 
exports keyword to make properties and methods available outside the module file
eg:

exports.myDateTime = function () {

  return Date();
};

Include your created module -
var http = require('http');

var dt = require('./myfirstmodule');

http.createServer(function (req, res) {

  res.writeHead(200, {'Content-Type': 'text/html'});
  
  res.write("The date and time are currently: " + dt.myDateTime());
  
  res.end();
  
}).listen(8080);

Node.js File System Module - 
Node.js file system module allows you to work with the file system on your computer
To include the File System module, use the require() method:

var fs = require('fs');

Uses of File System Module -
1. Read Files -
The fs.readFile() method is used to read files on your computer
2. Create Files -
The File System module has methods for creating new files:

fs.appendFile()
fs.open()
fs.writeFile()
3. Update Files -
The File System module has methods for updating files:

fs.appendFile()
fs.writeFile()

4. Delete Files -
To delete a file with the File System module,  use the fs.unlink() method

5. Rename Files
To rename a file with the File System module,  use the fs.rename() method

Node.js URL Module - 
The URL module splits up a web address into readable parts

To include the URL module, use the require() method:

var url = require('url');

Node.js Events -
Objects in Node.js can fire events, like the readStream object fires events when opening and closing a file

var events = require('events');
var eventEmitter = new events.EventEmitter();

