# node-red-contrib-alexa-home

[![Greenkeeper badge](https://badges.greenkeeper.io/mabunixda/node-red-contrib-alexa-home.svg)](https://greenkeeper.io/)

[![Build Status](https://travis-ci.org/mabunixda/node-red-contrib-alexa-home.svg?branch=master)](https://travis-ci.org/mabunixda/node-red-contrib-alexa-home)

The node just works wihtin your local network - no extra cloud stuff is required.

## Installation
Install directory from your Node-RED Settings Pallete

or

Install using npm

    $ npm install node-red-contrib-alexa-home


## Message Object Properties
the follow *msg* properties are generated within this node

**payload.on:** true|false

**payload.bri:** brightness 0-255

**payload.xy** Color XY object

**alexa_ip:** \<ip of alexa device interacting with node-red\>

With version 1.x now also the input is processed within the node and updates the data to alexa. Within the alexa app you are now able to get the current state of your nodes.


At the moment you can input as payload objects:
* [brightness](https://github.com/mabunixda/node-red-contrib-alexa-home/blob/master/alexa/alexa-home.js#L85)
* [color](https://github.com/mabunixda/node-red-contrib-alexa-home/blob/master/alexa/alexa-home.js#L79)
* [on/off](https://github.com/mabunixda/node-red-contrib-alexa-home/blob/master/alexa/alexa-home.js#L95)

Normal an input is not routed as output because this would possibly cause endless update loops. But if you want this and know what you are doing, you can set the [output param on the msg](https://github.com/mabunixda/node-red-contrib-alexa-home/blob/master/alexa/alexa-home.js#L133) to let the input passthrough.
