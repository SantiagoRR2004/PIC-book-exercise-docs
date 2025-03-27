# Gateway Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-GDA-\* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

I installed the java extensions from Visual Studio Code to make it work and installed maven doing "sudo apt install maven" in the terminal.
I had to add settings.json to the .vscode folder to make the logging appear in the DEBUG CONSOLE tab when a test is executed.

#### How does your implementation work?

I created a task that automatically downloads the extensions when the folder is opened with Visual Studio Code. The needed text was also added in the right places.

For the logging I also had to change from `_Logger.fine` to `_Logger.info` to make the logs appear in the DEBUG CONSOLE tab.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: [chapter01](https://github.com/SantiagoRR2004/PIC-java-components/tree/chapter01)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](../Java/src/test/java/programmingtheiot/part01/unit/common/ConfigUtilTest.java)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [GatewayDeviceAppTest](../Java/src/test/java/programmingtheiot/part01/integration/app/GatewayDeviceAppTest.java)

EOF.
