---
layout: post
title: Getting Started with Node.js & Express
postimg: /assets/uploads/pink-and-blue-geometric-technology-keynote.png
date: 2020-03-20T09:41:00.000Z
category: 'webdevelopment , javascript'
author: iamharsh
---
Hey folks! Welcome to my artcile on getting started with Node.js and express and today we will be learning WTF is Node.js and Express.js. So,without any further do let's get started.

# What is Node.js  ?

![nodejs](/assets/uploads/pink-and-blue-geometric-technology-keynote-1-.png)

Node.js is a JavaScript runtime environment. The Node run-time environment includes everything you need to execute a program written in JavaScript. As an asynchronous event-driven JavaScript runtime, Node.js is designed to build scalable network applications.

JavaScript now has the capability to do things that other scripting languages like Python can do.

Both your browser JavaScript and Node.js run on the V8 JavaScript runtime engine. This engine takes your JavaScript code and converts it into a faster machine code. Machine code is low-level code which the computer can run without needing to first interpret it.

## What Can Node.js Do?

* Node.js can generate dynamic page content

  Node.js can create, open, read, write, delete, and close files on the server

  Node.js can collect form data

  Node.js can add, delete, modify data in your database

## What is a Node.js File?

* Node.js files contain tasks that will be executed on certain events

  A typical event is someone trying to access a port on the server

  Node.js files must be initiated on the server before having any effect

  Node.js files have extension ".js"

## Installation

![](/assets/uploads/pink-and-blue-geometric-technology-keynote-2-.png)

Node.js can be installed in different ways. This post highlights the most common and convenient ones.

Official packages for all the major platforms are available at <https://nodejs.org/en/download/>.

One very convenient way to install Node.js is through a package manager. In this case, every operating system has its own.

On macOS, [Homebrew](https://brew.sh/) is the de-facto standard, and - once installed - allows to install Node.js very easily, by running this command in the CLI:

```sh
brew install node
```

Other package managers for Linux and Windows are listed in <https://nodejs.org/en/download/package-manager/>

## Lets create Hello World Node.js App

<!-- Copy and Paste Me -->

<div class="glitch-embed-wrap" style="height: 420px; width: 100%;">
  <iframe
    src="https://glitch.com/embed/#!/embed/experienced-fallacious-fireplant?path=server.js&previewSize=0&attributionHidden=true"
    title="experienced-fallacious-fireplant on Glitch"
    allow="geolocation; microphone; camera; midi; vr; encrypted-media"
    style="height: 100%; width: 100%; border: 0;">
  </iframe>
</div>

The code tells the computer to write "Lol Boi!" if anyone (e.g. a web browser) tries to access your computer on port 3000.

## How can i do the same ? 

* First of all install node.js on your machine. Tutorial mentioned above.

  First create a directory named myapp, change to it and run npm init. Then install express as a dependency   ```npm install express --save ``` .

In the myapp directory, create a file named server.js or whatever you like and copy in the code from the example above.

The req (request) and res (response) are the exact same objects that Node provides, so you can invoke req.pipe(), req.on('data', callback), and anything else you would do without Express involved.

Run the app with the following command:

```
$ node app.js
```

Then, load http://localhost:3000/ in a browser to see the output.

This was all about the basics of node.js and expreess framework and if you want to know more then do follow me on   [My Instagram](https://instagram.com/iamharsh.dev/) . Comment down your queries and thanks for reading till the end.