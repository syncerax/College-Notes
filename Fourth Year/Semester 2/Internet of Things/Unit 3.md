# Internet of Things

## Unit 3: Smart Objects: The "Things" in IoT

### Sensors

- Sensors measure some physical quantity (temperature, pressure, light, etc.) and convert them into a digital representation.
- This digital representation is passed to another device for conversion into useful data that can be consumed by intelligent devices or humans.
- Sensors can be easily embedded in any physical objects.
- If such host objects are connected to the Internet, they can communicate with other hosts, interpret their environment and make intelligent decisions.
- The different types of sensors are:

| Sensor Type               | Description                                                  | Example               |
| ------------------------- | ------------------------------------------------------------ | --------------------- |
| Position                  | Measures the position of an object.                          | Proximity sensor      |
| Occupancy and motion      | Occupancy sensors detect the presence of people/animals in a surveillance area. Motion sensors detect movement of people/objects. | Radar                 |
| Velocity and acceleration | Velocity sensors may be linear or angular. Acceleration sensors measure changes in velocity. | Accelerometer         |
| Force                     | Detect whether a physical force is applied and whether it is beyond a certain threshold. | Force gauge           |
| Pressure                  | Measure forces applied by liquids and gases.                 | Barometer             |
| Flow                      | Detect the rate of fluid flow.                               | Anemometer            |
| Acoustic                  | Measure sound levels, convert it into digital/analog signals. | Microphone            |
| Humidity                  | Detect humidity in air or a mass.                            | Hygrometer            |
| Light                     | Detect the presence of light (visible/invisible).            | Infrared sensor.      |
| Radiation                 | Detect radiation in the environment.                         | Geiger-Müller counter |
| Temperature               | Measure the amount of heat/cold in a system. 2 types: contact and non-contact. | Thermometer           |
| Chemical                  | Measure the concentration of chemicals in a system.          | Breathalyzer          |
| Biosensors                | Detect biological elements like enzymes, tissues, etc.       | Electrocardiograph    |

### Actuators

- Actuators are natural complements to sensors.
- They receive some type of control signal that triggers a physical effect, like some type of motion, force, etc.
- A processor can send an electric signal to an actuator, which translates that into some kind of motion (linear, rotational, etc) or some form of physical work.
- The different types of actuators are:

| Type                    | Examples                                        |
| ----------------------- | ----------------------------------------------- |
| Mechanical              | Lever, screw jack                               |
| Electrical              | Bipolar transistor, diode                       |
| Electromechanical       | DC motor, step motor                            |
| Electromagnetic         | Electromagnet                                   |
| Hydraulic and pneumatic | Hydraulic cylinder, pneumatic cylinder, piston  |
| Smart material          | Shape Memory Allow (SMA), piezoelectric bimorph |
| Micro and nano          | Microvalve                                      |

### Smart Objects

- They are the building blocks of IoT.
- They are what transform everyday objects into a network of intelligent objects that are able to learn from and interact with their environment in a meaningful way.
- The real power of smart objects comes from being networked together rather than being isolated as standalone objects.
- A smart device is one that has at least the following 4 characteristics:
  - **Processing unit:** A smart object has some type of processing unit for acquiring data, processing data received from sensors, sending control signals to actuators, etc.
  - **Sensor(s) and/or actuator(s):** A smart object is able to interact with the world through sensors and actuators.
  - **Communication device:** This is responsible for connecting the object with the outside world.
  - **Power source:** Smart objects have components that need a power source.

### Sensor Networks

- A sensor/actuator network (SANET) is a network of sensors that sense and measure their environment and/or actuators that act on their environment.
- SANETs offer highly coordinated sensing and actuating capabilities. Smart homes are a type of SANET that display this coordination between sensors and actuators.
- Advantages of a wireless solution:
  - Higher global flexibility
  - Lower implementation cost
  - Simpler scaling to a large number of nodes
  - Easier long term maintenance
- Disadvantages of a wireless solution:
  - Potentially less secure
  - Prone to impact/influence from the network
  - Lower transmission speeds

#### Wireless Sensor Networks

- Made up of wirelessly connected smart objects
- Limitations of smart objects in WSNs:
  - Limited processing power
  - Limited memory
  - Limited power
  - Limited transmission speeds
- Cost of nodes continues to decline, thus it is easier to deploy large numbers of nodes (redundancy). This gives better accuracy.
- Large numbers of nodes permit the introduction of node hierarchies. Hierarchies provide the ability to aggregate data from nearby sensor nodes.
- Data aggregation techniques help in reducing the amount of overall traffic in large WSNs.
- 2 communication patterns:
  - Event driven
  - Periodic

### Communications Criteria

#### Range

- How far does the signal need to be propagated?
- Should indoor and outdoor deployments be differentiated?
- To answer these questions, the simplest approach is to break these technologies into ranges:

| Name         | Range                                    | Example                                                      |
| ------------ | ---------------------------------------- | ------------------------------------------------------------ |
| Short range  | 10s of metres                            | Bluetooth, VLC                                               |
| Medium range | 10s to 100s of metres. Less than 1 mile. | IEEE 802.11 WiFi, IEEE 802.15.4, IEEE 802.15.4g WPAN. Wired: Ethernet |
| Long range   | Over 1 mile                              | Cellular: 2G, 3G, 4G                                         |

#### Frequency bands

- Licensed
- Unlicensed

#### Power consumption

- Powered nodes
- Battery powered nodes

#### Topology

| Range  | Topology                 |
| ------ | ------------------------ |
| Low    | Star                     |
| Medium | Star, mesh, peer-to-peer |
| High   | Star                     |

#### Constrained devices

According to RFC 7228, constrained devices can be categorised into:

- **Class 0:** Less than 10kb RAM, 100kb Flash processing and storage capacity. Cannot implement IP stack.
- **Class 1:** About 10kb RAM, 100kb Flash processing and storage capacity. Cannot implement IP stack. Can implement stack for CoAP.
- **Class 2:** More than 50kb RAM, 250kb Flash. They implement IP stacks.