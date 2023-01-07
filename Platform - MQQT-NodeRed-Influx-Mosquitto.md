# Platform - MQQT-NodeRed-Influx-Mosquitto.md
https://www.superhouse.tv/41-datalogging-with-mqtt-node-red-influxdb-and-grafana/

## Mosquitto
- sudo apt install mosquitto mosquitto-clients | install broker and client
- mosquitto_sub -v -t "#" | Subscribe to all Topics (-t "#") and in Verbose Mode (-v)

## InfluxDB
- Add Sources to Apt from Influx website key
- wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add - 
- echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
- sudo apt update
- Install InfluxDB and set to auto start on boot up
- sudo apt install influxdb
- sudo systemctl unmask influxdb
- sudo systemctl enable influxdb
- sudo systemctl start influxdb
- Create an username/password
- influx
- CREATE USER admin WITH PASSWORD 'adminpass' WITH ALL PRIVILEGES
- exit
- Tell Influex to use Account just created
- sudo nano /etc/influxdb/influxdb.config
- edit 4 lines in [http] section 
- [http]
- auth-enabled = true
- pprof-enabled = true
- pprof-auth-enabled = true
- ping-auth-enabled = true
- Save Changes and restart InfluxDB
- sudo systemctl restart influxdb
- Connecting to Influex with account
- influx -username admin -password adminpass
- Create database to store sensors
- CREATE DATABASE sensors


## Node-Red
- Do not use package version from apt but use install script
- sudo apt install build-essentail git
- bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
### The script will ask you a couple of questions about whether you are sure you want to proceed, and whether to install Pi-specific nodes. Say “y” (yes) to both questions.

### Node-RED can be extended by installing modules to give it extra features. We need to do that now so that it can connect to your InfluxDB database. Use NPM to install the InfluxDB nodes:

- npm install node-red-contrib-influxdbCopy
### At this point Node-RED is be installed, but just like with InfluxDB you need to configure it to be automatically started on boot:

- sudo systemctl enable nodered.serviceCopy
### You can start the service manually this time, but in future it will happen automatically when your Pi starts up:

- sudo systemctl start nodered.service

## Install Grafana
### Just like with InfluxDB, we can install Grafana by adding the official repository and installing the package. Start by fetching the public key for the repository and adding it to the local keyring:

- wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -Copy
- echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.listCopy
### Update the package list (again!) and install the Grafana package:

- sudo apt update
- sudo apt install grafanaCopy
### Just like the other packages we’ve installed, we need to enable the service so that it will start automatically:

- sudo systemctl enable grafana-serverCopy
### That takes care of starting Grafana at boot. For now, let’s start it manually:
- sudo systemctl start grafana-serverCopy

## Configure your sensors to send data to MQTT
For each sensor that you want to log and report, you will need to go through a series of steps to ensure that the data is received by your Raspberry Pi, processed by Node-RED, stored in InfluxDB, and then charted using Grafana. This is a process that you will repeat multiple times as your build up your home automation system.

### Let’s break it down into a series of simple steps.

###  Begin watching MQTT for messages. There won’t be any messages yet, but this is a handy technique for discovering new devices when they begin reporting to MQTT. On your Raspberry Pi, open a terminal and run the Mosquitto client command that we ran earlier:

- mosquitto_sub -u mqtt_username -P mqtt_password -v -t "#"Copy
### This launches the Mosquitto client in “verbose” mode (the “-v” flag) and subscribes to all topics using the wildcard character. What this means is the client will display every message that is published by any client to any topic, and report not just the message but also the topic that it appeared in.

###  The IP address (or hostname) of your MQTT broker. In this case, it’s the IP address of the Raspberry Pi.
###  The username and password for MQTT. We configured this way back at the start of the process. If you don’t have a username and password on your broker, you can skip this.
### The MQTT topics for reporting. In many devices this should default to something sensible, and you may not need to change it. For our Air Quality Sensor project, the topic will be generated automatically based on the chip ID of the ESP chip.
###  If you are using the example Arduino sketch for the Air Quality Sensor, open it in the Arduino IDE and go to the tab called “config.h”. Edit the broker ###  IP address and the MQTT username / password to match your own settings:



# Just commands
# Platform - MQQT-NodeRed-Influx-Mosquitto.md
https://www.superhouse.tv/41-datalogging-with-mqtt-node-red-influxdb-and-grafana/
 
- sudo apt install mosquitto mosquitto-clients
- mosquitto_sub -v -t "#"
 
- wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add - 
- echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
- sudo apt update
- sudo apt install influxdb
- sudo systemctl unmask influxdb
- sudo systemctl enable influxdb
- sudo systemctl start influxdb
- influx
- CREATE DATABASE sensors
- exit
- sudo apt install build-essentail git
- bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)

- npm install node-red-contrib-influxdbCopy

- sudo systemctl enable nodered.serviceCopy

- sudo systemctl start nodered.service

- wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -Copy
- echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.listCopy

- sudo apt update
- sudo apt install grafanaCopy

- sudo systemctl enable grafana-serverCopy
- sudo systemctl start grafana-serverCopy

- mosquitto_sub -u mqtt_username -P mqtt_password -v -t "#"Copy





## Optional credentials for InfluxDB
- influx
- CREATE USER admin WITH PASSWORD 'adminpass' WITH ALL PRIVILEGES
- exit
- Tell Influex to use Account just created
- echo "MANUAL WORK" !!!
- sleep
- sudo nano /etc/influxdb/influxdb.config
- [http]
- auth-enabled = true
- pprof-enabled = true
- pprof-auth-enabled = true
- ping-auth-enabled = true
- Save Changes and restart InfluxDB
- sudo systemctl restart influxdb
- Connecting to Influex with account
- influx -username admin -password adminpass
