# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-\* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

Now the constrained device application has a manager that monitors the CPU and memory of the device and loggs it at regular intervals.

#### How does your implementation work?

The SystemPerformanceManager creates instances of SystemCpuUtilTask and SystemMemUtilTask and uses them to log information about the CPU. The 2 classes inherit from an abstract class called BaseSystemUtilTask and they obtain the information by using the psutil library.

An instance SystemPerformanceManager is used by the ConstrainedDeviceApp to monitor the CPU and memory of the device.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter02](https://github.com/SantiagoRR2004/PIC-python-components/tree/chapter02)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py)
- [SystemCpuUtilTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.py)
- [SystemMemUtilTaskTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.py)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [ConstrainedDeviceAppTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py)
- [SystemPerformanceManagerTest](https://github.com/SantiagoRR2004/PIC-python-components/blob/main/src/test/python/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.py)

EOF.
