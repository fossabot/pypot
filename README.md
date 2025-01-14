[![PyPI](https://img.shields.io/pypi/v/pypot.svg)](https://pypi.python.org/pypi/pypot/)
[![Build Status](https://travis-ci.org/poppy-project/pypot.svg?branch=master)](https://travis-ci.org/poppy-project/pypot) [![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fdavidjsherman%2Fpypot.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fdavidjsherman%2Fpypot?ref=badge_shield)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.591809.svg)](https://doi.org/10.5281/zenodo.591809)



# Pypot: A Python lib for Dynamixel motors control

Pypot is a library developed in the [Inria FLOWERS](https://flowers.inria.fr/) team to make it easy and fast to control custom robots based on dynamixel motors. This framework provides different levels of abstraction corresponding to different types of use. More precisely, you can use pypot to:

* directly control robotis motors (both protocol v1 and v2 are supported) through a USB2serial device,
* define the structure of your particular robot and control it through high-level commands,
* define primitives and easily combine them to create complex behavior.

Pypot has been entirely written in Python to allow for fast development, easy deployment and quick scripting by non-necessary expert developers. It can also benefits from the scientific and machine learning libraries existing in Python. The serial communication is handled through the standard library and thus allows for rather high performance (10ms sensorimotor loop). It is crossed-platform and has been tested on Linux, Windows and Mac OS.

Pypot is also compatible with the [CoppeliaSim simulator](http://www.coppeliarobotics.com) (formerly V-REP). This allows you to seamlessly switch from a real robot to its simulated equivalent without having to modify your code.

Finally, it has been developed to permit an easy and fast extension to other types of motors and sensors.

## The Poppy-project: open source

Pypot is part of the [Poppy project](http://www.poppy-project.org) aiming at developing robotic creations that are easy to build, customize, deploy, and share. It promotes open-source by sharing hardware, software, and web tools.

At the moment we already proposed a few Poppy Creatures:

* the [Poppy Humanoid](https://github.com/poppy-project/poppy-humanoid): a kid-size humanoid robot designed for biped locomotion and physical human-robot interaction,
* a [Poppy Torso](https://github.com/poppy-project/poppy-torso): the humanoid torso, with a suction pad to install it on a desk
* and a [Poppy Ergo Jr](https://github.com/poppy-project/poppy-ergo-jr) with low-cost XL-320 robotis motors and modular 3D printed parts.

![Poppy Humanoid](./doc/poppy-creatures.jpg)

All those creatures are based on a combination of standard dynamixel actuators, 3D printed parts and open-source electronics such as Arduino boards. Both the hardware (3D models, electronics...) and software can be freely used, modified and duplicated.

## Documentation

The full pypot documentation on a html format can be found [here](https://docs.poppy-project.org/en/software-libraries/pypot.html). It provides tutorials, examples and a complete API.

## Installation

Pypot is a library entirely written in [Python](https://www.python.org). It works with Python *3.5+*. It is cross-platform and has been tested on Windows, Mac, Linux - yet specific usb to serial driver may be required depending on your system (see below).

You can build and install pypot with the typically python way:

```bash
cd pypot
pip install .
```

You will also have to install the driver for the USB2serial port. There are a few devices that have been tested with pypot that could be used:

* [USB2AX](http://www.xevelabs.com/doku.php?id=product:usb2ax:quickstart) - this device is designed to manage TTL communication only
* USB2Dynamixel - this device can manage both TTL and RS485 communication.
* [Pixl board](https://github.com/poppy-project/pixl) for RaspberryPi

For more details on the installation procedure, please refer to the [installation section](http://poppy-project.github.io/pypot/intro.html#installation) of the documentation.



## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fdavidjsherman%2Fpypot.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fdavidjsherman%2Fpypot?ref=badge_large)