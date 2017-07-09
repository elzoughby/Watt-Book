## Introduction

Internet of Things (IoT) is a sprawling set of technologies and use cases that has no clear, single definition. One workable view frames IoT as the use of network-connected devices, embedded in the physical environment, to improve some existing process or to enable a new scenario not previously possible.

These devices, or *things*, connect to the network to provide information they gather from the environment through sensors, or to allow other systems to reach out and act on the world through actuators. They could be connected versions of common objects we might already be familiar with, or new and purpose-built devices for functions not yet realized. They could be devices that we own personally and have on our persons or in our homes, or they could be embedded in factory equipment, or part of the fabric of the city we live in. Each of them is able to convert valuable information from the real world into digital data that provides increased visibility into how our users interact with our products, services, or applications.

The specific use cases and opportunities across different industries are numerous, and in many ways the world of IoT is just getting started. What emerges from these scenarios is a set of common challenges and patterns. IoT projects have additional dimensions that increase their complexity when compared to other cloud-centric technology applications, including:

- Diverse hardware.
- Diverse operating systems and software on the devices.
- Different network gateway requirements.

This chapter explains the elements we can combine with Firebase Cloud Platform to build a robust, maintainable and end-to-end IoT solution on Cloud Platform.

### Overview of the top level components

Here we divide the system into three basic components, the device, gateway, and cloud:

![Components of cloud-based IOT](img/IOTComponent.png)

A *device* includes hardware and software that directly interacts with the world. Devices connect to a network to communicate with each other, or to centralized applications. Devices might be directly or indirectly connected to the Internet.

A *gateway* enables devices that are not directly connected to the Internet to reach cloud services. Although the term *gateway* has a specific function in networking, it is also used to describe a class of device that processes data on behalf of a group or cluster of devices. The data from each device is sent to Cloud Platform, where it is processed and combined with data from other devices, and potentially with other business-transactional data. [1]

### Internet Of Things Architecture

Here is the detailed architecture design of the cloud-based Internet Of Things according to the top level components. [2]

![Internet Of Things Architecture](img/IOTArchitecture.jpg)

We have discussed in details the the *Cloud* and the *Gateway* components in the previous chapters. Here we will talk about the *Device* component at the left side of the previous figure. This chapter explains in details the construction of the *Device* component in the cloud-based Internet Of Things project for Watt?.

### Devices

It's not always clear what constitutes a device. Many physical things are modular, which means it can be hard to decide whether the whole machine is the device, or each module is a discrete device. There's no single, right answer to this question. As we design our IoT project, we'll need to think about the various levels of abstraction in our design and make decisions about how to represent the physical things and their relationships to each other. [1]

#### Embedded Systems

We have introduced the concept of the Internet of Things at a high level, defining the term and outlining its implications. Here we explore some of the details involved in the design and implementation of IoT devices. Unlike traditional computer-based systems, IoT devices are “embedded” within other devices in order to provide enhanced functionality without exposing the user to the complexities of a computer. The users interact with the device in a natural way, similar to their interactions with any other objects in the world. In this way, an embedded system has an interface that conforms to the expectations and needs of the users. Establishing a natural interface requires that the embedded system interface with the physical world directly through sensors, which read the state of the world, and actuators, which change the state of the world. Now we will discuss the structure of embedded systems and describe these interactions with the physical world.

As its name suggests, Embedded means something that is attached to another thing. An embedded system can be thought of as a computer hardware system having software embedded in it. An embedded system can be an independent system or it can be a part of a large system. An embedded system is a microcontroller or microprocessor based system which is designed to perform a specific task. For example, a fire alarm is an embedded system; it will sense only smoke.

#### Characteristics of an Embedded System

- **Single-functioned** An embedded system usually performs a specialized operation and does the same repeatedly. For example: A pager always functions as a pager.
- **Tightly constrained** All computing systems have constraints on design metrics, but those on an embedded system can be especially tight. Design metrics is a measure of an implementation's features such as its cost, size, power, and performance. It must be of a size to fit on a single chip, must perform fast enough to process data in real time and consume minimum power to extend battery life.
- **Reactive and Real time** Many embedded systems must continually react to changes in the system's environment and must compute certain results in real time without any delay.
- **Microprocessors based** It must be microprocessor or microcontroller based.
- **Memory** It must have a memory, as its software usually embeds in ROM. It does not need any secondary memories in the computer.
- **Connected** It must have connected peripherals to connect input and output devices.
- **Hardware/Software systems** Software is used for more features and flexibility. Hardware is used for performance and security.

#### Basic Structure of an Embedded System

Most of the Embedded systems found are composed of a **Hardware** and a **Software** embedded on the that hardware. So we can define an embedded system as a computer based, software driven, reliable and real-time control system.

## References

1. ["Overview of Internet of Things"](https://cloud.google.com/solutions/iot-overview). Google Cloud Platform. April 19, 2017. Retrieved July 7, 2017.
2. ["Intel steps into the Internet of platforms"](https://rickbouter.wordpress.com/2014/12/10/intel-steps-into-the-internet-of-platforms/). Intel® IoT Platform. 2014. Retrieved July 7, 2017.
3. ["Embedded Systems - Overview"](https://www.tutorialspoint.com/embedded_systems/es_overview.htm). Tutorialspoint. Retrieved July 7, 2017.