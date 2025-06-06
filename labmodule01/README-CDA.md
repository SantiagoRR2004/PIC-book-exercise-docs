# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-\* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

It automatically formats the entire repository with black for the python files and prettier for the JSON files. Using the extension [Gruntfuggly.triggertaskonsave](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.triggertaskonsave) it also formats automatically with black each time a file is saved. The implementation also automatically creates an environment in Visual Studio Code and downloads all the pip requirements.

[ConfigConst.py](../Python/src/main/python/programmingtheiot/common/ConfigConst.py) has been updated so the path to DEFAULT_CONFIG_FILE_NAME and DEFAULT_CRED_FILE_NAME is always absolute and it doesn't matter where the repository is installed.

To make the tests work I choose to modify the PYTHONPATH with the [.env](../Python/.env) file instead to having to export the PYTHONPATH each time the repository is installed.

I also made Visual Studio Code's Testing work by adding multiple `__init__.py` files and adding normal unnitest configurations in the settings.json file.

Later I changed the types of tests to pytest, so I could run tests in parallel.

#### How does your implementation work?

By using multiple Vscode configurations, I made everything work.

The pytest configuration is in the [pytest.ini](../Python/pytest.ini) file

### Code Repository and Branch

NOTE: Be sure to include the branch

URL: [chapter01](https://github.com/SantiagoRR2004/PIC-python-components/tree/chapter01)

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- [ConfigUtilTest](../Python/src/test/python/programmingtheiot/part01/unit/common/ConfigUtilTest.py)

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- [ConstrainedDeviceAppTest](../Python/src/test/python/programmingtheiot/part01/integration/app/ConstrainedDeviceAppTest.py)

EOF.
