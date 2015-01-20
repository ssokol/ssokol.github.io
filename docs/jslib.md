# Respoke Javascript Client Library

## Introduction

The Respoke JavaScript Client Library (respoke.js) is an open source library (MIT license). It provides the following features and functions:

* Live voice, video and phone calling
* User-to-user and group meassaging
* Screen sharing
* User (endpoint) presence
* Group presence (aka membership)
* Peer-to-peer data transfer
* User identity management

This library is built for use in web browsers and other HTML/CSS/JS-based environments (i.e. Node Webkit).

## Getting the Respoke Javascript Client Library

You can include the library in your projects in several ways. These include:

**1. Link To The Respoke CDN**

This is the easiest method and gives your application access to the most up-to-date version of the library. To include the current version of the library in your application, simply add a `<script>` tag as follows:

	<script src="https://cdn.respoke.io/respoke.min.js"></script>

This can be included in either the `head` or `body` section of your HTML document. If you need to link to a specific release of the library, you can find direct links to the various legacy versions [here](http://cdn.respoke.io/list.html).

**2. Download A Copy**

Linking to a copy on the CDN is generally the preferable, but you're also welcome to download a copy and host it on your own server.

**3. Install Locall Using npm**

If you're using Browserfy to manage your front-end build process, you can easily install a copy of the current library using npm:

	$ npm install --save --production respoke


## Using The Respoke Javascript Client Library

### Object Orientation

The library is object oriented and exposes a number of objects that allow your application to communicate in real time and to interact with the Respoke platform. When the library loads, it automatically creates an instance of a singleton object called `respoke` which serves as the starting point.

To create a connection to the Respoke platform, you will need to create an instance of the `connection` object using the `respoke` object's `createConnection()` method. For details on this process, please see the Quickstart Guide and the reference for the `respoke` object.

### Events, Callbacks and Promises

The library provides several methods for handling asynchronous functions. These include events, callbacks and promises.

[more on this]

### Development Mode vs. Production Mode

The library and the Respoke platform offer two operating modes: development and production. Development mode simplifies the process of building an application but is insecure by design. Production mode is secure but requires some effort on the part of the developer to configure.

#### Development Mode

Development mode makes it very simple to get started building an application by defaulting a number of security and permissions-related values and by foregoing the brokered access model. While in development mode, your client-side application code can:

* assert its own identity
* send messages to any other endpoint in the application
* place calls to any other endpoint in the application
* join any group in the application
* create new groups

#### Production Mode

