# Platform - MQQT-NodeRed-Influx-Mosquitto.md

## Mosquitto
- sudo apt install mosquitto mosquitto-clients | install broker and client
- mosquitto_sub -v -t "#" | Subscribe to all Topics (-t "#") and in Verbose Mode (-v)

## InfluxDB
- wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add - 
- echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
- sudo apt update
- sudo apt install influxdb
- sudo systemctl unmask influxdb
- sudo systemctl enable influxdb
- sudo systemctl start influxdb
