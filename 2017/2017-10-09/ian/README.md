# Capture Data with Asyncio
Links: [Github](https://github.com/irsbugs/meetings/blob/master/2017/2017-10-09/ian/README.md) or [Website](https://irsbugs.github.io/meetings/2017/2017-10-09/ian/) 

## The Cycle Analyst and Capturing its Serial Line data with Asyncio

The Cycle Analyst is a product that controls and monitors an electic-bike. It has the ability to output ttl serial data every second. The data string of containing 14 fields of status information.

A python server application captures the data. The asyncio module is used to capture the data and the pydbus module broadcasts it over the system D-Bus.

A python client application uses pydbus to capture the data. After analysis and filtering the data, espeak is used to output a spoken message.


## Update

While using asyncio supported the pydbus ability to publish data on the D-Bus, it was found that it would not support the pydbus method call feature. To support both features it is recommended to use GLib.MainLoop.


 

