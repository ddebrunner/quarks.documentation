---
layout: docs
title: Overview
description:  Quarks Overview
weight: 5
---

# Quarks Overview
Devices and sensors are everywhere, and more are coming online every day. You need a way to analyze all of the data coming from your devices, but it can be expensive to transmit all of the data from a sensor to your central analytics engine.

Quarks is an open source programming model and runtime for edge devices that enables you to analyze data and events at the device. When you analyze on the edge, you can:

* Reduce the amount of data that you transmit to your analytics server

* Reduce the amount of data that you store

A Quarks application uses analytics to determine when data needs to be sent to a back-end system for further analysis, action, or storage. For example, you can use Quarks to determine whether a system is running outside of normal parameters, such as an engine that is running too hot.

If the system is running normally, you don’t need to send this data to your back-end system; it’s an added cost and an additional load on your system to process and store. However, if Quarks detects an issue, you can transmit that data to your back-end system to determine why the issue is occurring and how to resolve the issue.   

Quarks enables you to shift from sending a continuous flow of trivial data to the server to sending only essential and meaningful data as it occurs. This is especially important when the cost of communication is high, such as when using a cellular network to transmit data, or when bandwidth is limited.

The following use cases describe the primary situations in which you would use Quarks:

* *Internet of Things (IoT):* Analyze data on distributed edge devices and mobile devices to:
  * Reduce the cost of transmitting data
  * Provide local feedback at the devices
* *Embedded in an application server instance:* Analyze application server error logs in real time without impacting network traffic
* *Server rooms and machine rooms:* Analyze machine health in real time without impacting network traffic or when bandwidth is limited

## Deployment environments
The following environments have been tested for deployment on edge devices:

* Java 8, including Raspberry Pi B and Pi2 B
* Java 7
* Android

## Edge devices and back-end systems
You can send data from a Quarks application to your back-end system when you need to perform analysis that cannot be performed on the edge device, such as:

* Running a complex analytic algorithm that requires more resources, such as CPU or memory, than are available on the edge device.
* Maintaining large amounts of state information about a device, such as several hours worth of state information for a patient’s
medical device.
* Correlating data from the device with data from other sources, such as:
  * Weather data
  * Social media data
  * Data of record, such as a patient’s medical history or trucking manifests
  * Data from other devices

Quarks communicates with your back-end systems through the following message hubs:

* MQTT – The messaging standard for IoT
* IBM Watson IoT Platform – A cloud-based service that provides a device model on top of MQTT
* Apache Kafka – An enterprise-level message bus
* Custom message hubs

Your back-end systems can also use analytics to interact with and control edge devices. For example:

* A traffic alert system can send an alert to vehicles that are heading towards an area where an accident occurred
* A vehicle monitoring system can reduce the maximum engine revs to reduce the chance of failure before the next scheduled service if it detects patterns that indicate a potential problem
