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
