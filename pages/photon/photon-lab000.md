---
layout: page-fullwidth
title: "Particle Photon IoT Labs: Getting Started"
subheadline: "A Step-by-Step Guide"
teaser: "This is a step-by-step guide to preparing your computer for the Particle Photon IoT Labs."
show_meta: true
comments: true
header: no
breadcrumb: true
categories:
    - iot-photon-labs
    - maker-101
author: "Doug Seven"
permalink: "/photon/00/"
---
### Table of Contents
*  Auto generated table of contents
{:toc}

## Preparing for the Particle Photon IoT Labs
The labs in this series build on each other to enable you to prototype your own Internet of Things (IoT) devices. In this lab you will build a solution using a 'Gateway' pattern, where a device (the Gateway) collects data from one or more connected devices/sensors and aggregates the data before sending it to the cloud. For the gateway, you will use Node.js and an open source framework for interacting with hardware, called Johnny-Five, which works as a baseline control kit for hardware projects, including the Particle Photon, Arduino and Raspberry Pi boards. This enables you to write applications in JavaScript that can run as a gateway either on your computer or on a hub device (like a Raspberry Pi 2) connected to an variety of devices.

<img src="/images/gatewaypattern.png"/>

We chose the Particle Photon for these labs because it is an inexpensive ($19) development kit that has a ARM-based System on a Chip (SoC) with Wi-Fi. The first part of this lab series will get you familiar with using input sensors and output devices with the Particle Photon. After that you will begin sending telemetry to the cloud and sending command and control back to the Photon. By the end of the lab series you will be able to build a gateway (aka hub-and-spoke) IoT solution with one or more Particle Photons as spoke devices connecting over Wi-Fi/TCP to a Raspberry Pi 2 as the hub (running the Node.js app that controls all of the spoke devices).

## Bill of Materials
To prepare your development environment for this lab series you don't need anything other than a computer. Each lab in the series will have a bill of materials indicating what is required for that lab.

If you want to prepare yourself further before the labs you can acquire the following:

1. [Particle Photon Development Kit - $29.00][1]
2. [Jumper wires - $1.95](https://www.sparkfun.com/products/12795)

## Install a Code Editor
If you don't already have one installed, pick a text/code editor. Feel free to use anything you like, provided it won't inject any extra text into your files.

Some Options:

* [Visual Studio Code][4] (this is our preferred tool)
* [Visual Studio][5]
* [Sublime Text][6] 
* [Eclipse][7] 
* [Notepad++][8]

## Install Node.js v0.12.7
In the labs you will write small programs that will run on your computer, connected to your Photon. These programs will be written in JavaScript and will be built on Node.js. If you are not familiar or experienced with Node.js, don't worry. You will learn everything you need to know for these labs in these labs. 

Follow the [instructions here to install Node.js](http://www.nodejs.org) on your computer.  __IMPORTANT:__ Be sure to install [version 0.12.x][node_12_7] - not version 4.0.

## Install Johnny-Five
Johnny-Five is an open source JavaScript framework that provides a simple object model for interacting with a variety of hardware boards and the sensors and devices you connect to them. 

Once you have Node.js installed, install [Johnny-Five][11] using NPM.
On Windows, open the Node.js command prompt and type the following:
<pre>
  npm install -g johnny-five
</pre>

On Mac OS X open Terminal and type the following:
<pre>
  sudo npm install -g johnny-five
</pre>

## Install Particle-CLI
The [Particle-CLI][3] is a command line interface for working with both the Particle Photon and the Particle Cloud. This tool will be used to 'claim' or provision your Photon, and may provide other useful benefits.

On Windows, open the Node.js command prompt and type the following:
<pre>
  npm install -g particle-cli
</pre>

On Mac OS X open Terminal and type the following:
<pre>
  sudo npm install -g particle-cli
</pre>

## Set Up a Development Directory
The last thing to do is prepare a place to save all of your work in the labs. I recommend an easy to navigate to directory with a relatively short path. Create a new folder/directory for the labs - I recommend:

### Windows
<pre>
  C:\Development\IoTLabs
</pre>

### Mac OS X
<pre>
  ~\Development\IoTLabs
</pre>

## Create a Free Particle Cloud Account
The Particle Photon is pre-configured to connect to the Particle Cloud. In order to 'claim' or provision the device, and to update its firmware (which you will do in [Lab 01][13]) you must create a free account with Particle Cloud. Go to [https://build.particle.io/signup][14] to create a new Particle Cloud account (make sure you remember your login email address and password - you will need it during this lab series).

## Create a Microsoft Azure Trial Account
In this lab series you will use Microsoft Azure as the cloud backend for your IoT solution. If you don't already have an Azure account, go to [https://azure.microsoft.com/en-us/pricing/free-trial/][15] to start a free trial of Microsoft Azure. You may need a credit card for identity verification, but the trial is completely free. If you have an MSDN Subscription you may be eligible for free credits to Microsoft Azure every month. Check your [MSDN account][16] page for details.

That's it for now. You are ready to start the [first set of labs][13].

{% include next-previous-post-in-category.html %}

 [1]: https://store.particle.io/?product=photon-kit
 [3]: http://www.particle.io/prototype#cli
 [4]: http://code.visualstudio.com
 [5]: http://www.visualstudio.com 
 [6]: http://www.sublimetext.com 
 [7]: http://www.eclipse.org/downloads/ 
 [8]: http://notepad-plus-plus.org/
 [9]: http://git-scm.com/
 [10]: http://nodejs.org/
 [11]: http://www.npmjs.com/package/johnny-five
 [12]: http://www.nitrogen.io
 [13]: /photon/01/
 [14]: https://build.particle.io/signup
 [15]: https://azure.microsoft.com/en-us/pricing/free-trial/
 [16]: https://msdn.microsoft.com/subscriptions/manage/
 [node_12_7]: https://nodejs.org/dist/v0.12.7/