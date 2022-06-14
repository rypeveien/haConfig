# home-assistant
My home assistant stuff

My installation runs on a Workstation with Debian Linux and software raid 
- CPU: Intel Core i3-9100
- Memory: 8 GB 
- Disks: 2x WDC WD20EZRZ-00Z5HB0 (2x2TB Sata)

Average power usage for the workstation is 35Watt

Dongles: 
- Aeotec Z-Stick Gen5 - zWave
- ConbeeII - Zigbee
- Bluetooth dongle
- RFXtrx433-controller

Home assistant, zigbee2mqtt and zwavejs2mqtt are run as docker-containers, using docker-compose

The following services are run as normal services, that are somehow used by HA: 
- dnsmasq - dns and dhcp-server
- mosquitto - mqtt-server
- mariadb-server - mysql-server for HA-recorder and other stuff useful to me

Home-brew services to communicate with home assistant
- dnsmasq_phone_detect - listen for dhcp-request from phone, and report them to HA, using MQTT
- pvlogger_2_ha - check if pvlogger is alive, and report solar production to HA

Integrations used by home-assistant
- Adax - controls my 3 panel heaters
- Amshan - reads my Tibber pulse through local MQTT
- Easee EV charger - charges my Hyundai Ioniq
- Mill - about to be replaced
- Netatmo - some weather information measured locally, but read from the cloud
- Shelly - various device
- tibber - not really used, as ai use tibber Pulse through AmsHan integration and fetches prices using rest api
- Xiaomi Miio - tries to controll my robotvac, but I guess the chinese monitors me instead
- zigbee and zWaveJS through MQTT

I try to save some money turning water heater and Car charger on and off, based on:
- What I get charged by my energy-provider (Tibber) (from 0-3NOK/kWh)
- What my local energy-grid company charges for delivery (0.36-0.56NOK/kWh) + monthly fee based on max hourly usage of some sort
- What my solar panels may generate, and what price I get for delivering to the grid 
- Added VAT and other fees to the community
- When do I need the car ready charged 
- When was the water heater last on a full cycle
- How many showers has been taken since last full cycle. 



