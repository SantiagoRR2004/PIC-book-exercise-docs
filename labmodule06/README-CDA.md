# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

In this chapter the capability to use publish/subscribe (pub/sub) data communications using MQTT for the Constrained Device Application was implemented. To implement this, mosquitto and wireshark were installed. Wireshark in particular is used for testing the MQTT communications.

#### How does your implementation work?

The most important class for this chapter is [MqttClientConnector](../Python/src/main/python/programmingtheiot/cda/connection/MqttClientConnector.py). It uses the [paho-mqtt](https://pypi.org/project/paho-mqtt/) library to subscribe and publish messages to different topics. The [DeviceDataManager](../Python/src/main/python/programmingtheiot/cda/app/DeviceDataManager.py) class uses the connector to subscribe and unsubscribe to the `ResourceNameEnum.CDA_ACTUATOR_CMD_RESOURCE` topic.

To install Mosquitto, the following command was run:

```bash
sudo apt install mosquitto mosquitto-clients
```

To test the code with Wireshark, first Wireshark is installed. Then it needs to be opened with root privilage in Linux.

```bash
sudo apt install wireshark
sudo wireshark
```

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter06](https://github.com/SantiagoRR2004/PIC-python-components/tree/chapter06)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](../Python/src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py)
- [SystemCpuUtilTaskTest](../Python/src/test/python/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.py)
- [SystemMemUtilTaskTest](../Python/src/test/python/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.py)
- [SystemDiskUtilTaskTest](../Python/src/test/python/programmingtheiot/part01/unit/system/SystemDiskUtilTaskTest.py)
- [SystemNetIntUtilTaskTest](../Python/src/test/python/programmingtheiot/part01/unit/system/SystemNetIntUtilTaskTest.py)
- [SystemNetOutUtilTaskTest](../Python/src/test/python/programmingtheiot/part01/unit/system/SystemNetOutUtilTaskTest.py)
- [ActuatorDataTest](../Python/src/test/python/programmingtheiot/part02/unit/data/ActuatorDataTest.py)
- [SensorDataTest](../Python/src/test/python/programmingtheiot/part02/unit/data/SensorDataTest.py)
- [SystemPerformanceDataTest](../Python/src/test/python/programmingtheiot/part02/unit/data/SystemPerformanceDataTest.py)
- [HumiditySensorSimTaskTest](../Python/src/test/python/programmingtheiot/part02/unit/sim/HumiditySensorSimTaskTest.py)
- [PressureSensorSimTaskTest](../Python/src/test/python/programmingtheiot/part02/unit/sim/PressureSensorSimTaskTest.py)
- [TemperatureSensorSimTaskTest](../Python/src/test/python/programmingtheiot/part02/unit/sim/TemperatureSensorSimTaskTest.py)
- [HumidifierActuatorSimTaskTest](../Python/src/test/python/programmingtheiot/part02/unit/sim/HumidifierActuatorSimTaskTest.py)
- [HvacActuatorSimTaskTest](../Python/src/test/python/programmingtheiot/part02/unit/sim/HvacActuatorSimTaskTest.py)
- [DataUtilTest](../Python/src/test/python/programmingtheiot/part02/unit/data/DataUtilTest.py)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [ConstrainedDeviceAppTest](../Python/src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py)
- [SystemPerformanceManagerTest](../Python/src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py)
- [SensorAdapterManagerTest](../Python/src/test/python/programmingtheiot/part02/integration/system/SensorAdapterManagerTest.py)
- [ActuatorAdapterManagerTest](../Python/src/test/python/programmingtheiot/part02/integration/system/ActuatorAdapterManagerTest.py)
- [DeviceDataManagerNoCommsTest](../Python/src/test/python/programmingtheiot/part02/integration/app/DeviceDataManagerNoCommsTest.py)
- [SenseHatEmulatorQuickTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/SenseHatEmulatorQuickTest.py)
- [HumidityEmulatorTaskTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/HumidityEmulatorTaskTest.py)
- [PressureEmulatorTaskTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/PressureEmulatorTaskTest.py)
- [TemperatureEmulatorTaskTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/TemperatureEmulatorTaskTest.py)
- [HumidifierEmulatorTaskTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/HumidifierEmulatorTaskTest.py)
- [HvacEmulatorTaskTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/HvacEmulatorTaskTest.py)
- [LedDisplayEmulatorTaskTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/LedDisplayEmulatorTaskTest.py)
- [SensorEmulatorManagerTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/SensorEmulatorManagerTest.py)
- [ActuatorEmulatorManagerTest](../Python/src/test/python/programmingtheiot/part02/integration/emulated/ActuatorEmulatorManagerTest.py)
- [DataIntegrationTest](../Python/src/test/python/programmingtheiot/part02/integration/data/DataIntegrationTest.py)
- [RedisClientAdapterTest](../Python/src/test/python/programmingtheiot/part02/integration/connection/RedisClientAdapterTest.py)
- [MqttClientConnectorTest](../Python/src/test/python/programmingtheiot/part03/integration/connection/MqttClientConnectorTest.py)
- [MqttClientControlPacketTest](../Python/src/test/python/programmingtheiot/part03/integration/connection/MqttClientControlPacketTest.py)

EOF.
