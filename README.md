# Home Assistant At SnM Nest

This provides the yaml configuration used at SnM Nest Home Assistant. 

![resourceslist](images/HomeAutomation.png "Home automation Diagram")

# Devices

- Hass.io running in Docker in a Ubuntu VM. Ubuntu VM is running a Hyper-V host. 
- Vera Edge for Z-Wave Control
- Xiaomi Gateway
- Philips Hue Bridge Gen 2
- Philips Lights
- Philips Light Strips
- Xiaomi Human Motion Sensors
- Xiaomi Door Sensors
- Xiaomi Temperature Sensor
- Xiaomi Buttons
- Xiaomi Plug
- Google Home Hubs
- Google Hub Minis
- Amazon Alexa 
- Logitech Harmony
- Advantage Air 
- Fibaro Dimmers
- AeoTec MultiSensor 6 Gen5
- AeoTec Smart Switch
- UniFi Network Switch
- UniFi Access Point - NanoHD
- UniFi Secure Gateway
- UniFi G3 Flex Camera


# CI/CD - DevOps

DevOps was implemented with Azure DevOps. Only continuous delivery is configured. Below diagram provides a high level overview of the configuration. For more details around the configuration please visit the [blog post](https://sameeraman.wordpress.com/2018/12/10/local-self-hosted-agents-in-azure-devops/). 


![resourceslist](images/cicd.png "Home automation Diagram")

# Dashboards

![resourceslist](images/dashboard-crop.png "Home automation Diagram")