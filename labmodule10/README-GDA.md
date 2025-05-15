# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

#### How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter10](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter10)

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

### GDA MQTT Client Performance Test Results

#### `testConnectAndDisconnect`

```text
abr 24, 2025 9:48:17 A. M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
abr 24, 2025 9:48:18 A. M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
abr 24, 2025 9:48:18 A. M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
abr 24, 2025 9:48:18 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest testConnectAndDisconnect
INFORMACIÓN: Connect and Disconnect [1]: 416 ms
```

#### `testPublishQoS0`

```text
abr 24, 2025 9:51:00 A. M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
abr 24, 2025 9:51:00 A. M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
abr 24, 2025 9:51:01 A. M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
abr 24, 2025 9:51:01 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: \n\tTesting Publish: QoS = 0 | msgs = 10000 | payload size = 212 | start = 1.7454811E9 | end = 1.7454811E9 | elapsed = 1.272
abr 24, 2025 9:51:01 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: Publish message - QoS 0 [10000]: 1272 ms
```

#### `testPublishQoS1`

```text
abr 24, 2025 9:51:48 A. M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
abr 24, 2025 9:51:48 A. M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
abr 24, 2025 9:51:49 A. M. programmingtheiot.gda.connection.MqttClientConnector publishMessage
abr 24, 2025 9:51:50 A. M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
abr 24, 2025 9:51:50 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: \n\tTesting Publish: QoS = 1 | msgs = 10000 | payload size = 212 | start = 1.7454811E9 | end = 1.7454811E9 | elapsed = 1.493
abr 24, 2025 9:51:50 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: Publish message - QoS 1 [10000]: 1493 ms
```

#### `testPublishQoS2`

```text
abr 24, 2025 9:54:00 A. M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
abr 24, 2025 9:54:00 A. M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
abr 24, 2025 9:54:03 A. M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
abr 24, 2025 9:54:03 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: \n\tTesting Publish: QoS = 2 | msgs = 10000 | payload size = 212 | start = 1.7454812E9 | end = 1.7454812E9 | elapsed = 2.383
abr 24, 2025 9:54:03 A. M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: Publish message - QoS 2 [10000]: 2383 ms
```

#### Results

The connect and disconnect test took 416 ms, while the publish tests took the following times:

- QoS 0: 1272 ms
- QoS 1: 1493 ms
- QoS 2: 2383 ms

As expected, the QoS 0 test was the fastest, while the QoS 2 test was the slowest. The QoS 1 test was in between. This is consistent with the expected behavior of MQTT, where higher QoS levels introduce more overhead due to message acknowledgment and delivery guarantees.

EOF.
