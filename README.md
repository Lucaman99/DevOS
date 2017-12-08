# DevOS

An online operating system emulator, geared towards code development.

Coded In:
  - HTML
  - CSS
  - Javascript and jQuery
  - Eventually, other languages and libraries such as PHP, SQL, and Node.js will hopefully be added
  
At the moment, DevOS uses labelled cookies to remember its data (it is only meant to remember local data), but hopefully Node.js and SQL will allow for information to be stored in a more efficient way. 

In this version, DevOS runs completely on cookies, and in all versions pushed to this repository, cookies will be used to store all information, until further notice. This method of storage is incredibly inconsistent, and at the current time, I am working on implementing a MySQL server, acessed by either Node.js or PHP to store data.

In order to use this code right now, follow these steps:

First, the user must install Node.js on their computer. It can be found via this link: https://nodejs.org/en/. Next, after Node.js is downloaded and installed, the user must open up their command line and type the following:

```npm install http``` and then after this command has run, ```npm install fs```.

The user can then open up a text editor file, and call it initialize.js (or whatever name the user wants, but in these instructions, it will be called initialize.js). They will then put this code into the text editor:

```
var http = require('http');
var fs = require('fs');

http.createServer(function(req, res){
    fs.readFile("DevOS.html", function(err, data){
        res.writeHead(200, {"Content-Type": "text/html"});
        res.write(data);
        res.end();
    })
}).listen(//Insert port number here);
```
> Note, this code was edited and modified by myself, but the original code was not created by me. 

The user can then take the code within this repository, and save it as another file. In initialize.js, I have called the file DevOS.html, but the user can call it whatever they want, as long as they are sure to change the name of the file within initialize.js. Finally, the user will save all of this code into one location. In this demonstration, I will save the code to a file on my desktop called CompiledDevOS. In the command line, the user can then type: ```cd Desktop/CompiledDevOS```. After this code has run, the user will type: ```node initialize.js```. The command line will begin to run this code. Do not terminate the command line, just leave it running, while you want to use the code. In the portion of initialize.js, where it says: "Inser port number here", the user can change this to the localhost port number that they want the code to run through. They can then navigate to this port that they have chosen, with http://localhost:port-number, and the code should be running.

This code will also work with the LivePreview on Adobe Brackets. Beyond that, I have not tested anything else. When using the localhost, the user must remember that whenever they want to run the code, they have to type ```cd Desktop/CompiledDevOS```, and then ```node initialize.js``` in order for the code to be hosted on the localhost. The user may have to refresh the code a few times to get the cookies working, as this code is still in its early stages, and is quite buggy.


