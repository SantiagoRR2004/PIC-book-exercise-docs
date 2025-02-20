# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-\* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

In the constrained device application the ability to simulate sensors and actuators was implemented. Some classes we created to store the data for the sensors and actuators. In this chapter managers are created to be in charge of the the sensors and actuators. There is a manager that controls the sensor manager, the actuator manager and the CPU information manager. These middle managers are prepared to handle simulated and emulated sensors and actuators.

#### How does your implementation work?

The implementation works by using inheritance between classes and managers that control objects. The BaseActuatorSimTask and BaseSensorSimTask are classes that are inherited by the actuators and sensors and that have the functions required to create simulated data with ActuatorData and SensorData respectively. The children of BaseActuatorSimTask are HumidifierActuatorSimTask and HvacActuatorSimTask. The children of BaseSensorSimTask are HumiditySensorSimTask, PressureSensorSimTask and TemperatureSensorSimTask. The different simulated sensors are used by SensorAdapterManager to periodically generate data. The actuator children are used by ActuatorAdapterManager to send messages to them or set a listener. These 2 managers are programmed in a generic way that allow them to work with emulated sensors and actuators in the future. Those 2 manager plus SystemPerformanceManager are finally controlled by the DeviceDataManager.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter03](https://github.com/SantiagoRR2004/PIC-python-components/tree/chapter03)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py)
- [SystemCpuUtilTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.py)
- [SystemMemUtilTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.py)
- [ActuatorDataTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/data/ActuatorDataTest.py)
- [SensorDataTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/data/SensorDataTest.py)
- [SystemPerformanceDataTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/data/SystemPerformanceDataTest.py)
- [HumiditySensorSimTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/sim/HumiditySensorSimTaskTest.py)
- [PressureSensorSimTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/sim/PressureSensorSimTaskTest.py)
- [TemperatureSensorSimTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/sim/TemperatureSensorSimTaskTest.py)
- [HumidifierActuatorSimTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/sim/HumidifierActuatorSimTaskTest.py)
- [HvacActuatorSimTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/unit/sim/HvacActuatorSimTaskTest.py)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [ConstrainedDeviceAppTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py)
- [SystemPerformanceManagerTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py)
- [SensorAdapterManagerTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/integration/system/SensorAdapterManagerTest.py)
- [ActuatorAdapterManagerTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/integration/system/ActuatorAdapterManagerTest.py)
- [DeviceDataManagerNoCommsTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part02/integration/system/DeviceDataManagerNoCommsTest.py)

EOF.
