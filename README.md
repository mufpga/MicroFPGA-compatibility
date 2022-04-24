<a href="https://mufpga.github.io/"><img src="https://raw.githubusercontent.com/mufpga/mufpga.github.io/main/img/logo_title.png" alt="Overview"/>

</a>

![version](https://img.shields.io/badge/version-3.1-blue)[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)



# Overview

MicroFPGA is an FPGA-based platform for the electronic control of microscopes. It aims at using affordable FPGA to generate or read signals from a variety of devices, including cameras, lasers, servomotors, filter-wheels, etc. It can be controlled via [Micro-Manager](https://micro-manager.org/MicroFPGA), or its [Java](https://github.com/mufpga/MicroFPGA-java), [Python](https://github.com/mufpga/MicroFPGA-py) and [LabView](https://github.com/mufpga/MicroFPGA-labview) communication libraries, and comes with optional complementary [electronics](https://github.com/mufpga/MicroFPGA-electronics).

Documentation and tutorials are available on [https://mufpga.github.io/](https://mufpga.github.io/).



<img src="https://raw.githubusercontent.com/mufpga/mufpga.github.io/main/img/figs/G_overview.png" alt="Overview"/>

## Content

This repository contains the source related to discontinued boards and versions. It is updated to maintain back-compatibility for laboratory using the old boards. 

- v1 is the original Mojo code.
- v3 is updated following changes in the main [MicroFPGA repository](https://github.com/mufpga/MicroFPGA).
- A 17bits branch exists to maintain a version of the FPGA configuration compatible with a different type of servomotors.

Compiled configurations are available in the [releases](https://github.com/mufpga/MicroFPGA-mojo/releases). Instructions on how to build from source are available on the [project's website](https://mufpga.github.io/2_installing_microfpga.html). 



<!---

## Cite us

Deschamps J, Kieser C, Hoess P, Deguchi T and Ries J, 

--->

MicroFPGA-mm was written by Joran Deschamps, EMBL (2020).







This repository contains the Alchitry projects and Micro-Manager device adapters for V1 and v2:

- v1: the original MicroMojo, kept here for back compatibility.
- v3: a version compatible with MicroFPGA, including the newest features such as active camera trigger. 

For more details on how to build and use MicroFPGA or Mojo v3, refer to the [project homepage](https://mufpga.github.io).


MicroMojo and MicroFPGA were written by Joran Deschamps, EMBL (2020).
