Registration no.: 22MIC0132
Name: Sruti Samantaray

# Smart Home MQTT Publish–Subscribe System

## Overview
This project implements a Smart Home monitoring system using **Node-RED** and the **Mosquitto MQTT broker**.  
It demonstrates the publish–subscribe architecture, wildcard subscriptions, and Quality of Service (QoS) levels with real-time dashboard visualization.

---

## System Architecture

The system consists of:

- **Two Publishers**
  - Temperature Sensor → `home/livingroom/temperature`
  - Light Sensor → `home/bedroom/light`

- **Status Publisher**
  - Device Status → `home/livingroom/status`

- **One Wildcard Subscriber**
  - Subscribes to: `home/#`

- **MQTT Broker**
  - Mosquitto (running on localhost:1883)

- **Dashboard**
  - Built using Node-RED Dashboard nodes
  - Displays live data (Gauge, Chart, Text)

---

## Publish–Subscribe Model

- Publishers send data to specific topics.
- The MQTT broker routes messages based on topic hierarchy.
- The wildcard subscriber (`home/#`) receives all subtopics under the `home` namespace.
- A Switch node filters messages to appropriate dashboard widgets.

---

## Dashboard Components

### Living Room
- 🌡 Temperature Gauge
- 🟢 Device Status (Text Display)

### Bedroom
- 💡 Light Intensity Line Chart
 
