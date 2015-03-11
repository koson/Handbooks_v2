#SDK 

**Copied from http://developer.mbed.org/handbook/mbed-SDK**

#The mbed SDK

The mbed Software Development Kit (SDK) is a C/C++ microcontroller software platform relied upon by tens of thousands of developers to build projects fast. We've worried about creating and testing startup code, C runtime, libraries and peripheral APIs, so you can worry about coding the smarts of your next product.

The SDK is licensed under the permissive Apache 2.0 licence, so you can use it in both commercial and personal projects with confidence.

The mbed SDK has been designed to provide enough hardware abstraction to be intuitive and concise, yet powerful enough to build complex projects. It is built on the low-level ARM CMSIS APIs, allowing you to code down to the metal if needed. In addition to RTOS, USB and Networking libraries, a cookbook of hundreds of reusable peripheral and module libraries have been built on top of the SDK by the mbed Developer Community.


##Hello World!

Startup code, check. C Library integration, check. Peripheral libraries, check. We've worked hard to help you get to the point:

[Import the code](/teams/mbed/code/mbed_blinky/)


	#include "mbed.h"
 
	DigitalOut myled(LED1);
 
	int main() {
    	while(1) {
        		myled = 1;
        		wait(0.2);
        		myled = 0;
        		wait(0.2);
    	}
	}


##High-level Peripheral APIs

The mbed SDK gives you an API-driven approach to microcontroller coding.

We've done all the hard work of implementing drivers for the different [mbed platforms](/platforms), so you don't have to. It is liberating to fire up an interface, knowing it'll just work!

You can code using meaningful abstract objects and API calls, so you don't need to learn the microcontroller hardware details to get going. There is even a "Hello World!" example for every peripheral, just to get you started before you know it.

Take a look at some of these interfaces to get a feel of how it works: [digital out](/DigitalOut), [analog in](/Analogin), [SPI](/spi), [USB mouse](/USBMouse), [Timer](/timer), [CAN](/can).

But if needed, you can always bypass the APIs and talk directly to the microcontroller hardware using the low-level Cortex Microcontroller Software Interface Standard (CMSIS) APIs. Ideal when they are fine for most of your project, but one aspect needs specific low-level control.

For all the mbed C/C++ SDK APIs, see the [mbed handbook](/handbook)

To read more about mbed SDK coding style, see the [mbed SDK coding style](https://mbed.org/teams/SDK-Development/wiki/mbed-sdk-coding-style)

![logos](/2_Dev_Fun/Images/sdk_logos.png)

##Support for Multiple Targets

The abstraction provided by the mbed SDK APIs enables libraries and example code to be reused by any microcontroller target that the mbed SDK targets.

##Support for Multiple Toolchains

Our goal with the mbed Compiler and mbed SDK is to enable a consistent and stable fully integrated development platform that just works. This helps provide a consistent context for development, code sharing, and questions and answers with other developers that helps you be more productive, especially when prototyping.

However, the mbed C/C++ SDK used with the mbed Online Compiler is also compatible with a number of other popular ARM microcontroller toolchains!

If you'd like to use the [mbed platforms](/platforms) or mbed C/C++ SDK with an alternate tool, or simply migrate to one as your project develops past prototype, you can choose to export an mbed project to the toolchain of your choice by right-clicking on them in the IDE.

You can read more about this on the [Exporting to offline toolchains](/handbook//Exporting-to-offline-toolchains) handbook page.

##Open Source

![open source](/2_Dev_Fun/Images/sdk_open_source.png)

The mbed SDK is licensed under the permissive Apache 2.0 open source licence.

We wanted to make sure the license we chose made it possible to use the SDK in both commercial and personal projects with confidence, including no obligations to open source your own code if you didn't want to. Whilst we encourage sharing of code and experience to be reusable by others, we certainly don't want to enforce it, and a permissive license provides that freedom for our users to keep the options open.

If you are interested in delving in the depth of the mbed SDK implementation you can take a look at the documentation of the [mbed library internals](/handbook/mbed-library-internals).

and you can use the mbed library sources, instead of one of its builds:
[Import the code](/users/mbed_official/code/mbed-src/)

If you are interested in [porting the mbed SDK](/handbook/mbed-SDK-porting) to a new target we provide the sources of all the official mbed libraries, tests and [tools (build and test system)](/handbook/mbed-tools) in [this github repository](https://github.com/mbedmicro/mbe).

##See also
Check out the rest of the mbed platform, and [explore](http://mbed.org/explore/) what it can do for you!