## :warning: Important: The Mojo FPGA has unfortunately been discontinued. Their successors are based on a slightly different architecture and we are working on adapting the code for the new generation.


# MicroMojo

MicroMojo is intended as a platform for the control of different elements on custom microscopes. It is based on a low-price [FPGA](https://en.wikipedia.org/wiki/Field-programmable_gate_array "Wikipedia") (Field-Programmable Gate Array) called the [Mojo](https://embeddedmicro.com/products/mojo-v3 "Mojo V3") (Embedded Micro). To facilitate the use of MicroMojo in microscopes, a device adapter for [Micro-manager](https://micro-manager.org/ "Micro-manager website") is available in addition to the firmware.

# Why using a FPGA?

As opposed to most microcontrollers (such as the Arduino), FPGAs can carry on multiple tasks in parallel due to their architecture. While the Arduino is a great solution for simple tasks, it is rapidly overwhelmed when required to process signals rapidly. A good example for such a task - and the original motivation for MicroMojo - is to pulse in the microsecond range several lasers in a synchronous way. This can be achieved easily for one laser by an Arduino DUE, but becomes impossible with several lasers or requires multiple Arduino boards and synchronization signals. A FPGA can achive this task for many lasers without effort. Finally, the MojoFPGA comes at a comparable price to the Arduinos, making it an excellent choice for cheap integrated electronics in experimental set-ups. 

# What can MicroMojo do?

By design, MicroMojo offers out of the box several control signals useful in microscopy:

| Signal           | Details           | Use examples  |
| :--------------: |:-------------:| :-----:|
| Laser triggering | Using a camera read-out signal, multiple lasers can be triggered by a TTL (On/Off, pulsing with us resolution, follow the camera) | Laser triggering |
| TTL              | On/Off signal      |  Flip-mirrors  |
| Servos           | 1 ms - 2 ms servo signal      | Filter-wheel, moveable elements |
| PWM              | 0-100%      | Wiht a low-pass circuit: AOM %, laser % |
| Analog read-out  | 8 analog read-out channels      | Sensor read-outs |

For more details, please consult the [wiki](https://github.com/jdeschamps/MicroMojo/wiki).

# Micro-manager

[Micro-manager](https://micro-manager.org/ "Micro-manager website") is an open-source microscope control software, with a large set of compatible commercial devices. The communication with each device is done through a so-called device adapter. MicroMojo device adapter offers the possibility to load the desired number of each signal controller (LaserTrigger, TTL, Servo, PWM, AnalogReadOut) in the software. 

The device adapter needs to be compiled for a specific version of Micro-manager. Pre-compiled versions of the adapter will be made available for Micro-manager 1.14.23 and 2.

# Precautions

> **Caution**: the MojoFPGA runs on 3.3V, do not supply signals with higher voltage.

In addition, the MojoFPGA has a limited capacity in driving multiple servos at the same time. When using MicroMojo to control multiple servos, prefer supplying the driving voltage from a different source or supply an additional 5V power to the MojoFPGA.

See the [wiki](https://github.com/jdeschamps/MicroMojo/wiki) for tips in wiring.

# Wiki

The [wiki](https://github.com/jdeschamps/MicroMojo/wiki) is currently under construction.

# Outlook

A standalone Java program to run MicroMojo is being developed, as well as Micro-manager plugin and LabView program.


Joran Deschamps, EMBL, 2018
