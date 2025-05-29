# Gateway Device Application (Connected Devices)

## Lab Module 12 - Semester Project - GDA Components

Be sure to implement all the PIOT-GDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

For this implementation a new sensor and actuator had to be added. The new sensor is the grade given by a PIC exam and the actuator opens a PIC test in the browser to practice more PIC. The GDA recieves the data from the CDA and when 5 exams in a row have been failed it sends a trigger to the GDA to open the PIC test in the browser.

#### How does your implementation work?

In the [DeviceDataManager](../Java/src/main/java/programmingtheiot/gda/app/DeviceDataManager.java) a new function called `handleGradeSensorAnalysis` was created. When the sensor data arrives it checks to activate the actuator or not. The new configuration is in [PiotConfig](../Java/config/PiotConfig.props) and in [ConfigConst](../Java/src/main/java/programmingtheiot/common/ConfigConst.java).

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter12](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter12)

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
- [CloudClientConnectorTest](../Java/src/test/java/programmingtheiot/part04/integration/connection/CloudClientConnectorTest.java)

EOF.
