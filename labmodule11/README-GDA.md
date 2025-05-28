# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

A connection to the cloud is now implemented. The service used is [Ubidots](https://industrial.ubidots.com/).

#### How does your implementation work?

[CloudClientConnector](../Java/src/main/java/programmingtheiot/gda/connection/CloudClientConnector.java) is the class that connects to the cloud. It implements [ICloudClient](../Java/src/main/java/programmingtheiot/gda/connection/ICloudClient.java) and [IConnectionListener](../Java/src/main/java/programmingtheiot/gda/connection/IConnectionListener.java). The CloudClientConnector is used in the [DeviceDataManager](../Java/src/main/java/programmingtheiot/gda/app/DeviceDataManager.java) to send data to the cloud the same way as all other clients. All the CloudClientConnector configuration is stored in the [PiotConfig](../Java/config/PiotConfig.props) file, including how to connect to Ubidots.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter10](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter11)

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
- [MqttClientPerformanceTest](../Java/src/test/java/programmingtheiot/part03/integration/connection/MqttClientPerformanceTest.java)
- [DeviceDataManagerSimpleCdaActuationTest](../Java/src/test/java/programmingtheiot/part03/integration/app/DeviceDataManagerSimpleCdaActuationTest.java)

EOF.
