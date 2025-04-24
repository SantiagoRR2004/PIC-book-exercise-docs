# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-\* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

#### What does your implementation do?

#### How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL:

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

-
-
-

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

-
-
-

### CDA MQTT Client Performance Test Results

#### `testConnectAndDisconnect`

```text
2025-04-24 09:29:38,341:root:DEBUG:Config: ['Mqtt.GatewayService', 'Coap.GatewayService', 'ConstrainedDevice', 'Data.GatewayService']
2025-04-24 09:29:38,341:root:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x70adc894a840>
2025-04-24 09:29:38,341:root:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-04-24 09:29:38,341:root:INFO:      MQTT Broker Host: localhost
2025-04-24 09:29:38,341:root:INFO:      MQTT Broker Port: 1883
2025-04-24 09:29:38,341:root:INFO:      MQTT Keep Alive:  60
2025-04-24 09:29:38,341:root:INFO:MQTT client connecting to broker at host: localhost
2025-04-24 09:29:38,345:root:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x70adb023dbe0>
2025-04-24 09:29:39,345:root:INFO:Disconnecting MQTT client from broker: localhost
2025-04-24 09:29:39,346:root:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x70adb023dbe0>
2025-04-24 09:29:39,346:root:INFO:Connect and Disconnect: 905.27463 ms
```

#### `testPublishQoS0`

```text
2025-04-24 09:37:57,483:root:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-04-24 09:37:57,483:root:INFO:      MQTT Broker Host: localhost
2025-04-24 09:37:57,483:root:INFO:      MQTT Broker Port: 1883
2025-04-24 09:37:57,483:root:INFO:      MQTT Keep Alive:  60
2025-04-24 09:37:57,483:root:INFO:MQTT client connecting to broker at host: localhost
2025-04-24 09:37:57,487:root:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x703b56b0c200>
2025-04-24 09:37:57,487:root:INFO:Created DataUtil instance.
2025-04-24 09:37:57,488:root:DEBUG:Encoding SensorData to JSON [pre] -->SensorData [value=0.0]
2025-04-24 09:37:57,488:root:DEBUG:Encoding SensorData to JSON [post] -->{
    "timeStamp": "2025-04-24T07:37:57.487763+00:00",
    "hasError": false,
    "name": "Not Set",
    "typeID": 0,
    "statusCode": 0,
    "latitude": 0.0,
    "longitude": 0.0,
    "elevation": 0.0,
    "locationID": "constraineddevice001",
    "value": 0.0
}
2025-04-24 09:37:58,337:root:INFO:Disconnecting MQTT client from broker: localhost
2025-04-24 09:37:59,338:root:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x703b56b0c200>
2025-04-24 09:37:59,338:root:INFO:
        Testing Publish: QoS = 0 | msgs = 10000 | payload size = 264 | start = 1745480277488196.0 | end = 1745480278337507.0 | elapsed = 0.849310907
2025-04-24 09:37:59,338:root:INFO:Publish message - QoS 0 [10000]: 849.310907 ms
```

#### `testPublishQoS1`

```text
2025-04-24 09:40:30,947:root:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-04-24 09:40:30,948:root:INFO:      MQTT Broker Host: localhost
2025-04-24 09:40:30,948:root:INFO:      MQTT Broker Port: 1883
2025-04-24 09:40:30,948:root:INFO:      MQTT Keep Alive:  60
2025-04-24 09:40:30,948:root:INFO:MQTT client connecting to broker at host: localhost
2025-04-24 09:40:30,950:root:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x7276d9b1c8c0>
2025-04-24 09:40:30,951:root:INFO:Created DataUtil instance.
2025-04-24 09:40:30,951:root:DEBUG:Encoding SensorData to JSON [pre] -->SensorData [value=0.0]
2025-04-24 09:40:30,951:root:DEBUG:Encoding SensorData to JSON [post] -->{
    "timeStamp": "2025-04-24T07:40:30.951113+00:00",
    "hasError": false,
    "name": "Not Set",
    "typeID": 0,
    "statusCode": 0,
    "latitude": 0.0,
    "longitude": 0.0,
    "elevation": 0.0,
    "locationID": "constraineddevice001",
    "value": 0.0
}
2025-04-24 09:40:32,578:root:INFO:Disconnecting MQTT client from broker: localhost
2025-04-24 09:40:33,579:root:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x7276d9b1c8c0>
2025-04-24 09:40:33,579:root:INFO:
        Testing Publish: QoS = 1 | msgs = 10000 | payload size = 264 | start = 1745480430951372.5 | end = 1745480432578017.2 | elapsed = 1.6266448089999999
2025-04-24 09:40:33,579:root:INFO:Publish message - QoS 1 [10000]: 1626.644809 ms
```

#### `testPublishQoS2`

```text
2025-04-24 09:41:17,531:root:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-04-24 09:41:17,531:root:INFO:      MQTT Broker Host: localhost
2025-04-24 09:41:17,531:root:INFO:      MQTT Broker Port: 1883
2025-04-24 09:41:17,531:root:INFO:      MQTT Keep Alive:  60
2025-04-24 09:41:17,532:root:INFO:MQTT client connecting to broker at host: localhost
2025-04-24 09:41:17,534:root:INFO:Created DataUtil instance.
2025-04-24 09:41:17,535:root:DEBUG:Encoding SensorData to JSON [pre] -->SensorData [value=0.0]
2025-04-24 09:41:17,535:root:DEBUG:Encoding SensorData to JSON [post] -->{
    "timeStamp": "2025-04-24T07:41:17.534820+00:00",
    "hasError": false,
    "name": "Not Set",
    "typeID": 0,
    "statusCode": 0,
    "latitude": 0.0,
    "longitude": 0.0,
    "elevation": 0.0,
    "locationID": "constraineddevice001",
    "value": 0.0
}
2025-04-24 09:41:17,535:root:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x7db1507d3b90>
2025-04-24 09:41:19,817:root:INFO:Disconnecting MQTT client from broker: localhost
2025-04-24 09:41:20,818:root:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x7db1507d3b90>
2025-04-24 09:41:20,818:root:INFO:
        Testing Publish: QoS = 2 | msgs = 10000 | payload size = 264 | start = 1745480477535217.8 | end = 1745480479817021.8 | elapsed = 2.281804029
2025-04-24 09:41:20,818:root:INFO:Publish message - QoS 2 [10000]: 2281.804029 ms
```

#### MQTT Results

The connect and disconnect test took 905.27463 ms, while the publish tests took the following times:

- QoS 0: 849.310907 ms
- QoS 1: 1626.644809 ms
- QoS 2: 2281.804029 ms

As expected, the QoS 0 test was the fastest, while the QoS 2 test was the slowest. The QoS 1 test was in between. This is consistent with the expected behavior of MQTT, where higher QoS levels introduce more overhead due to message acknowledgment and delivery guarantees.

### CDA CoAP Client Performance Test Results

#### `testGetRequestCon`

```text
Received test ids from temp file.
testGetRequestCon (src.test.python.programmingtheiot.part03.integration.connection.CoapClientPerformanceTest.CoapClientPerformanceTest.testGetRequestCon)
Comment the annotation to perf test CON GET ... Testing GET - CON

GET message - useCON = True [10000]: 35173.175996 ms
ok
```

#### `testGetRequestNon`

```text
Received test ids from temp file.
testGetRequestNon (src.test.python.programmingtheiot.part03.integration.connection.CoapClientPerformanceTest.CoapClientPerformanceTest.testGetRequestNon)
Comment the annotation to perf test NON GET ... Testing GET - NON

GET message - useCON = False [10000]: 33680.407327 ms
ok
```

#### `testPostRequestCon`

```text
Received test ids from temp file.
testPostRequestCon (src.test.python.programmingtheiot.part03.integration.connection.CoapClientPerformanceTest.CoapClientPerformanceTest.testPostRequestCon)
Comment the annotation to perf test CON POST ... Testing POST - CON

POST message - useCON = True [10000]: 32593.874654 ms. Payload Len: 264
ok
```

#### `testPostRequestNon`

```text
Received test ids from temp file.
testPostRequestNon (src.test.python.programmingtheiot.part03.integration.connection.CoapClientPerformanceTest.CoapClientPerformanceTest.testPostRequestNon)
Comment the annotation to perf test NON POST ... Testing POST - NON

POST message - useCON = False [10000]: 32346.401918 ms. Payload Len: 264
ok
```

#### `testPutRequestCon`

```text
Received test ids from temp file.
testPutRequestCon (src.test.python.programmingtheiot.part03.integration.connection.CoapClientPerformanceTest.CoapClientPerformanceTest.testPutRequestCon)
Comment the annotation to perf test CON PUT ... Testing PUT - CON

PUT message - useCON = True [10000]: 33484.645943 ms. Payload Len: 264
ok
```

#### `testPutRequestNon`

```text
Received test ids from temp file.
testPutRequestNon (src.test.python.programmingtheiot.part03.integration.connection.CoapClientPerformanceTest.CoapClientPerformanceTest.testPutRequestNon)
Comment the annotation to perf test NON PUT ... Testing PUT - NON

PUT message - useCON = False [10000]: 33481.26746 ms. Payload Len: 264
ok
```

#### CoAP Results

The percentage difference between CON and NON is:

- GET: 4.43%
- POST: 0.77%
- PUT: 0.01%

The fastest was the POST request without CON, taking 32593.874654 ms, while the slowest was the GET request with CON, taking 35173.175996 ms. All tests that required confirmation (CON) were slower than those that did not. This is consistent with the expected behavior of CoAP, where CON messages require additional round trips for acknowledgment, leading to increased latency.

EOF.
