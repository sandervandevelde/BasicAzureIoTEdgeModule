# BasicAzureIoTEdgeModule

This module does not WORK!

Why? I don't know...

I tried to roll it out on both 1.2 and 1.1 (version 0.0.2 is build with this setting https://docs.microsoft.com/en-us/azure/iot-edge/how-to-vs-code-develop-module?view=iotedge-2018-06#set-iot-edge-runtime-version)


## Test scenarios

I tested this in several ways.

## Setup 1

Setup 1 is:
- actual Device
- Ubuntu 20.04LTS
- IoT Edge 1.3 runtime
- edgeAgent 1.3 and edgeHub 1.3
- Module svelde/iot-edge-basic-ingest:0.0.3-amd64
- See also deployment.manifest - Scenario1.json file

outcome: negative

```
adminsv@uv20:~$ iotedge logs -f basicingest
IoT Hub module client created. (for 1.1 runtime)
IoT Hub module client started.
One or more device twin desired properties changed:
{"a":42,"$version":2}
Sent current time as reported property to device twin
SetDesiredPropertyUpdateCallback one-time executed
SetDesiredPropertyUpdateCallback attached
SetInputMessageHandler 'input1' attached
Received Body: [{"machine":{"temperature":22.187675974768435,"pressure":1.1353048578850116},"ambient":{"temperature":21.0160127964411,"humidity":26},"timeCreated":"2022-07-18T09:43:20.4944342Z"}]
Received message sent
Received Body: [{"machine":{"temperature":22.187675974768435,"pressure":1.1353048578850116},"ambient":{"temperature":21.0160127964411,"humidity":26},"timeCreated":"2022-07-18T09:43:20.4944342Z"}]
Received message sent
```