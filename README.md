# Urbanova Cloud Iot Connection Kit Samples

Samples are provided as part of the Urbanova Cloud IoT Connection Kit to provide developers with examples of how to use the Urbanova IoT SDK to connect their devices and publish/subsribe to Urbanova Cloud projects.

To experiment with these samples you will need an Urbanova Cloud Account (currently in Alpha).

### Getting Started

#### Linux/Python

From your Urbanova Cloud account, add a new Data Source, select the `Internet of Things / Urbanova IoT SDK` option.

From the IoT Data Source configuration options, choose Connection Kit, and click the 'Download Urbanova Cloud IoT Connection Kit for Linux/Python' link.

This connection kit provides the deviceId, endpoint url, keys and certificates required to connect and IoT device to Urbanova Cloud using the Urbanova IoT SDK.  To configure and test device connectivity and message publishing to your Urbanova Project, perform the following steps:

* Note: Steps below assumes `git` is installed on the device and can be used to fetch dependencies from Urbanova and AWS GitHub repos.

##### Step 1: Unzip the connection kit on your IoT device (Linux/Python)

    ```$ unzip UrbanovaIotConnectionKit.zip```

##### Step 2:  Add execution permissions to the init.sh script

    ```$ chmod +x init.sh```

##### Step 3: Run the init.sh script

    ```$ ./init.sh```

The init script will download the AWS IoT SDK (this is required for secure IoT MQTT client connection to Urbanova Cloud using TLSv1.2 Mutual Authentication), and the samples contained in this repo with `git clone ...`.  The init script will then automatically start the `urbanovacloud/iotsdk/samples/helloSensor.py` example.

“Hello Sensor" messages sent from your device will now be published and available from your Data Source to be used in projects.  You can view the messages by clicking on the data source configuration and selecting the Unit Test tab.
