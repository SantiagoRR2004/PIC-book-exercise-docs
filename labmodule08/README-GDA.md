# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

In this chapter a basic CoAP sever was implemented. It has multiple handlers and only the PUT method was implemented.

#### How does your implementation work?

The most important class for this chapter is [CoapServerGateway](../Java/src/main/java/programmingtheiot/gda/connection/CoapServerGateway.java). It uses the [Eclipse Californium](https://eclipse.dev/californium/) library to create a CoAP server. The [DeviceDataManager](../Java/src/main/java/programmingtheiot/gda/app/DeviceDataManager.java) class creates, starts and stops the CoAP server. The server uses multiple handlers: one for the actuator commands [GetActuatorCommandResourceHandler](../Java/src/main/java/programmingtheiot/gda/connection/handlers/GetActuatorCommandResourceHandler.java), another for the telemetry [UpdateTelemetryResourceHandler](../Java/src/main/java/programmingtheiot/gda/connection/handlers/UpdateTelemetryResourceHandler.java) and another for the system performance data [UpdateSystemPerformanceResourceHandler](../Java/src/main/java/programmingtheiot/gda/connection/handlers/UpdateSystemPerformanceResourceHandler.java). The three handlers are made from the generic class [GenericCoapResourceHandler](../Java/src/main/java/programmingtheiot/gda/connection/handlers/GenericCoapResourceHandler.java) which implements the CoAP Resource interface.

To install Californium, a script that runs automatically when the proyect is opened in Visual Studio Code was created. If VSCode is not used, the script [buildCalifornium](../Java/buildCalifornium.sh) can be used.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter08](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter08)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](../Java/src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java)
- [SystemCpuUtilTaskTest](../Java/src/test/java/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.java)
- [SystemMemUtilTaskTest](../Java/src/test/java/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.java)
- [SystemDiskUtilTaskTest](../Java/src/test/java/programmingtheiot/part01/unit/system/SystemDiskUtilTaskTest.java)
- [SystemNetInUtilTaskTest](../Java/src/test/java/programmingtheiot/part01/unit/system/SystemNetInUtilTaskTest.java)
- [SystemNetOutUtilTaskTest](../Java/src/test/java/programmingtheiot/part01/unit/system/SystemNetOutUtilTaskTest.java)
- [ActuatorDataTest](../Java/src/test/java/programmingtheiot/part02/unit/data/ActuatorDataTest.java)
- [SensorDataTest](../Java/src/test/java/programmingtheiot/part02/unit/data/SensorDataTest.java)
- [SystemPerformanceDataTest](../Java/src/test/java/programmingtheiot/part02/unit/data/SystemPerformanceDataTest.java)
- [SystemStateDataTest](../Java/src/test/java/programmingtheiot/part02/unit/data/SystemStateDataTest.java)
- [DataUtilTest](../Java/src/test/java/programmingtheiot/part02/unit/data/DataUtilTest.java)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [GatewayDeviceAppTest](../Java/src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java)
- [SystemPerformanceManagerTest](../Java/src/test/java/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.java)
- [DataIntegrationTest](../Java/src/test/java/programmingtheiot/part02/integration/data/DataIntegrationTest.java)
- [DeviceDataManagerNoCommsTest](../Java/src/test/java/programmingtheiot/part02/integration/app/DeviceDataManagerNoCommsTest.java)
- [RedisClientAdapterTest](../Java/src/test/java/programmingtheiot/part02/integration/connection/RedisClientAdapterTest.java)
- [MqttClientConnectorTest](../Java/src/test/java/programmingtheiot/part03/integration/connection/MqttClientConnectorTest.java)
- [MqttClientControlPacketTest](../Java/src/test/java/programmingtheiot/part03/integration/connection/MqttClientControlPacketTest.java)
- [CoapServerGatewayTest](../Java/src/test/java/programmingtheiot/part03/integration/connection/CoapServerGatewayTest.java)

EOF.
