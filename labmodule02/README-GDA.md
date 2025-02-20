# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-\* issues.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

Now the system monitors the CPU and memory of the device and logs it at regular intervals.

#### How does your implementation work?

It is achieved by using multiple classes and java.lang.management.OperatingSystemMXBean.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter02](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter02)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](https://github.com/SantiagoRR2004/PIC-java-components/blob/main/src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java)
- [SystemCpuUtilTaskTest](https://github.com/SantiagoRR2004/PIC-java-components/blob/main/src/test/java/programmingtheiot/part01/unit/system/SystemCpuUtilTaskTest.java)
- [SystemMemUtilTaskTest](https://github.com/SantiagoRR2004/PIC-java-components/blob/main/src/test/java/programmingtheiot/part01/unit/system/SystemMemUtilTaskTest.java)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [GatewayDeviceAppTest](https://github.com/SantiagoRR2004/PIC-java-components/blob/main/src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java)
- [SystemPerformanceManagerTest](https://github.com/SantiagoRR2004/PIC-java-components/blob/main/src/test/java/programmingtheiot/part01/integration/system/SystemPerformanceManagerTest.java)

EOF.
