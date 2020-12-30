# ATS
Automated Test System for ROS2 version Autoware (Autoware architecture proposal and Autoware.Auto).

# Goals of this system
* Deploy ODD base on Autoware to specified hardware continuously and improve the stability.
* Simplifies the process for mass deployment and upgrade.
* Detect the performance changes of above S&H stack during iteration.

# Get start

[Installation instructions](https://github.com/autocore-ai/ats-script/blob/main/docs/install.md)

[How to use](https://github.com/autocore-ai/ats-script/blob/main/README.md)

# Docker-based framework
Target image combination for testing
| image name | contents in image |
| --- | --- |
| Runtime	| ROS foxy + dependents on runtime |
| Exe		| Autoware exe built for target runtime |
| Data		| Config\model\data for different scenario or function |
| Test		| Test contents for different scenario or function |

* Runtime is host image and others are volumes mounted to host image
* Runtime varies with different hardware and with independent version rarely changes
* Runtime install dev packages as building image which used to build Exe

# Current target hardware

* [AutoCore PCU 2.0](https://github.com/autocore-ai/autocore_pcu_doc)
* [Adlink MVP-6100-MXM](https://www.adlinktech.com/Products/Industrial_PCs_Fanless_Embedded_PCs/ExpandableFanlessEmbeddedComputers/MVP-6100-MXM_Series)
* [Jetson AGX Xavier](https://www.nvidia.cn/autonomous-machines/embedded-systems/jetson-agx-xavier/)

# Docker images
## env
Environment images includes runtime and devel image test system needed.
## exe
Executable images relay on env image.

# Test Report

[Automated Test System Reports](https://autocore-ai.github.io/ats-report/report.html)

# Road Map

* ROS2 porting
* Performance test
* Deploy into container
* Test Autoware nodes
* Localization test case

# Change Log