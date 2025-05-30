# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

As a consequence of not working on the Gateway Device Application (GDA) in chapters 3 and 4 a mix of different tasks were implemented. The main one was the translation between different types of data to JSON and back. Other things were making sure everything returns the correct information and that the classes are linked correctly.

Extra: A Redis database was added so that the Gateway device stores and retrieves the sensor, actuator and system performance data. The manager of different devices subscribes to this database.

#### How does your implementation work?

The DataUtil class can now transform ActuatorData, SensorData and SystemPerformanceData to and from JSON. The setters and getters from ActuatorData, SensorData, SystemPerformanceData and SystemStateData were completed and/or improved. GatewayDeviceApp was updated to use DeviceDataManager instead of SystemPerformanceManager.

Extra: The [RedisPersistenceAdapter](../Java/src/main/java/programmingtheiot/gda/connection/RedisPersistenceAdapter.java) class was created. It has functionalities to connect, disconnect and store and retrieve data in the Redis database. Some information for the connection was added to PiotConfig.props. It uses JedisPool to make sure that it can connect when using multiple threads. DeviceDataManager now extends JedisPubSub and has an instance of RedisPersistenceAdapter to be able to handle incoming messages. The test RedisClientAdapterTest was implemented to test the functionalities of RedisPersistenceAdapter.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter05](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter05)

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

EOF.
