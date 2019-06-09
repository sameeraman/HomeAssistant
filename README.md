# Home Assistant At SnM Nest

This provides the yaml configuration used at SnM Nest Home Assistant. If you are interested in trying out Home Assistant please visit the web site [here](https://www.home-assistant.io/)

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
- Yamaha RX-V473
- Ring Doorbell
- Sonos Connect Amp
- Sonos Play:3
- RainMachine Pro-8 for Sprinkler Control

# CI/CD - DevOps

DevOps was implemented with Azure DevOps. Only continuous delivery is configured. Below diagram provides a high level overview of the configuration. For more details around the configuration please visit the [blog post](https://sameeraman.wordpress.com/2018/12/10/local-self-hosted-agents-in-azure-devops/). 


 ![resourceslist](images/CICD.png "Home Assistant CI/CD")

# Dashboards

Following are some of the Lovelace Dashboards I have created to control the smart home. 

![resourceslist](images/dashboard-crop.png "Home automation Diagram")

![resourceslist](images/dashboard-living.png "Home automation Diagram")

![resourceslist](images/dashboard-camera.png "Home automation Diagram")

# Automations

Following are some of the automation that I'm using at my smart home. 

## Air conditioner Automation

- Set Air conditioner stop timer to 90 mins when it is turned on
- Reset Air Conditioner Stop Timer to 0 when the air conditioner is turned off  
- Turn on the Air conditioner on Weekdays at 06:15AM if the kitchen temperature is below 19C
- Alert when Air conditioner is left on for more than 4 hours
- Alert when Air conditioner is left on for more than 6 hours
- Alert and Turn off air conditioner if it is left On when the house alarm is on (After leaving home)

## Bathroom Automations
- Turn on the Bath Light when there is motion
- Turn off the Bath Light when there's no motion in shower and Bathroom
- Turn on the Bath strip when there is motion in master bedroom
- Turn off the Bath strip when there's no motion in master bedroom
- Alert every day at 10:00pm if any of the doors were left open

## Kitchen and Living Automations
- Turn on the Pantry Light when the door opens
- Turn off the Pantry light when the door close
- Turn off the Pantry Light when the door open and left for more than 2 minutes
- Turn on the Kitchen light then there is motion based on light and sunset
- Turn off the Kitchen Light when there is no motion for more than 10 minutes
- Turn on the living mood dim lights (light strips and lamps) when there is motion in kitchen/living and when time is between sunset and midnight
- Turn off the living mood dim lights at mid night
- Turn off the Living Sonos (if playing) when the TV is switched on
- Toggle Living Mood lights when Xiaomi Living push button is single pressed
- Toggle Living Sonos when Xiaomi Living push button is double pressed
- Alarm when there is motion outside master bedroom and when the night mood is on

## Garage Automation
- Turn on the Garage light then there is motion
- Turn off the Garage light then there is no motion
- Alert if the Garage door was left open for more than 10 minutes
- Alert if the Garage door was left open for more than 60 minutes
- Turn on the Front Outdoor light for 2 mins then there the garage door open
- Turn off the Garage light if it was one for more than 60 minutes

## Alfresco Automation
- Toggle Alfresco Sonos Music Play with Alfresco Xiaomi push button
- Jump to Next track in Alfresco Music Play when Alfresco Xiaomi push button double press is detected
- Turn on Alfresco Music Play with Alfresco Motion
- Turn off Alfresco Music Play with Alfresco No Motion for 5 mins
- Toggle Alfresco Automation with Alfresco Xiaomi push button long press
- Turn on Alfresco light with 20% when there is motion in Alfresco
- Turn off the Alfresco Light when there is no motion
- Alert if the Alfresco Sonos was playing for more than 2 hours
- Alert and Turn off if the Alfresco Sonos was playing for more than 4 hours

## Office Automations
- Turn on the Office light then there is motion
- Turn off the Office Light when there is no motion 
- Turn off the Office AC Vent when there is no motion for more than 5 minutes in the office
- Turn On the Office AC Vent when there is motion for more than 3 minutes in the office

## Master Bedroom Automations
- Turn off the Master Light when there is no motion for more than 5 minutes
- Turn on Bed Heater at 10pm if the master bedroom temperature is below 22C
- Turn off Bed Heater automatically after two hours

## Other Automations
- Send Alerts from Xiaomi Motion and Door sensors when the house is Armed
- Alert if the Laundry door was left open for more than 10 minutes
- Alert if the Laundry door was left open for more than 60 minutes
- Turn on house alarm based on device tracker - Arm when every one is out of the house
- Turn off house alarm based on device tracker - Unarm when anyone is back at home
- Turn on the night mood at midnight when there is no motion in the house
- Turn off the Night mood when master bedroom door open in the morning