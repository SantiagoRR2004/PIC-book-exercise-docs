# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

In this chapter the capability to use publish/subscribe (pub/sub) data communications using MQTT for the Constrained Device Application was implemented. Mosquitto and Wireshark are already installed the last chapter.

#### How does your implementation work?

The most important class for this chapter is [MqttClientConnector](../Java/src/main/java/programmingtheiot/gda/connection/MqttClientConnector.java). It uses the [Eclipse Paho](https://central.sonatype.com/artifact/org.eclipse.paho/org.eclipse.paho.client.mqttv3) library to subscribe and publish messages to different topics. The [DeviceDataManager](../Java/src/main/java/programmingtheiot/gda/app/DeviceDataManager.java) class uses the connector to subscribe and unsubscribe to the following list of topics:

- `ResourceNameEnum.GDA_MGMT_STATUS_MSG_RESOURCE`
- `ResourceNameEnum.CDA_ACTUATOR_RESPONSE_RESOURCE`
- `ResourceNameEnum.CDA_SENSOR_MSG_RESOURCE`
- `ResourceNameEnum.CDA_SYSTEM_PERF_MSG_RESOURCE`

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter07](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter07)

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

EOF.
