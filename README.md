# Urbanova Cloud Iot Connection Kit Samples

Samples are provided as part of the Urbanova Cloud IoT Connection Kit to provide developers examples of how to use the Urbanova IoT SDK to connect publish/subsribe endpoints to Urbanova Cloud.

To experiment with samples you will need an Urbanova Cloud Account (currently in Alpha).

### Getting Started

#### Linux/Python

From your Urbanova Cloud account, create a new Data Source, select `Internet of Things / Urbanova IoT SDK`

From the IoT Data Source configuration options, choose Connection Kit and click the 'Download Urbanova Cloud IoT Connection Kit for Linux/Python' link

This connection kit establishes secure connection to Urbanova Cloud (Alpha) using the AWS IoT SDK.  To configure and test device connectivity and message publishing to your Urbanova Project, perform the following steps:

* Note: Steps below assumes `git` is installed on the device and can be used to fetch dependencies from GitHub.

##### Step 1: Unzip the connection kit on your IoT device (Linux/Python)

    ```$ unzip UrbanovaIotConnectionKit.zip```

##### Step 2:  Add execution permissions to the init.sh script

    ```$ chmod +x init.sh```

##### Step 3: Run the init.sh script

    ```$ ./init.sh```

The init script will download the AWS IoT SDK (required for IoT MQTT client connection to Urbanova Cloud using TLSv1.2 Mutual Authentication) and samples contained in this repo using `git clone ...`.  The init script will then automatically start the `urbanovacloud/iotsdk/samples/helloSensor.py` example.

“Hello Sensor" messages sent from your device will now appear in your Projects that you have added the Data Source and can be viewed from the Test tab in the Data Source configuration settings.