# Internet of Things

## Unit 1: Introduction to Internet of Things

### What is the Internet of Things?

#### Overview

- The **Internet has experienced significant growth** in the past four decades, evolving from a network of a few hundred hosts to a platform capable of linking billions of entities globally.
- The **next evolution is to connect all “things”** that have (or will soon have) embedded wireless (or wired) connectivity **to control systems** that support data collection, data analysis, decision-making, and (remote) actuation.
- **“Things” include**, but are not limited to, machinery, home appliances, vehicles, individual persons, animals and habitats.
- This **new paradigm seeks to enhance** the traditional Internet into a smart *Internet of Things* (IoT) created around intelligent interconnections of diverse objects in the physical world.
- In the IoT, commonly deployed **devices contain an embedded device or microprocessor that can be accessed by some communication mechanism**, typically utilizing wireless links.

#### Applications

- **Industries** like automotive and fleet management, telecommunications, energy and utilities, security and defense, etc. **are in the process of deploying IoT services**. Proponents say that the IoT will usher in an **age of smart applications** and services that will help us cope with a variety of daily challenges.
- A short **list of applications** includes:
  - Things on the move
    - Retail
    - Logistics
    - Pharmaceuticals
    - Food
  - Ambient and assisted living
    - Health
    - Intelligent homes
    - Transportation
  - Ubiquitous intelligent devices
  - Pollution and disaster avoidance




- **Logistics** aims at improving the efficiency of existing processes. The **warehouses** of the future **will become automated**, with items being checked in and checked out and orders being placed automatically to suppliers. **Food may be transported** from producer to consumer **without human intervention**.

#### 4 pillars of IoT (IoT enabling technologies)

1. **M2M/MTC**: the "internet of devices"
2. **RFID**: the "internet of objects"
3. **WSN**: the "internet of transducers"
4. Supervisory Control and Data Acquisition (**SCADA**): the "internet of controllers"

#### Areas of Development and Standardization

- **Despite significant advances** in the underlying technology areas, there are **difficulties associated** with the evaluation of real-world IoT solution deployments. This is **due to the lack of standardization**.
- **Standards** covering many of the underlying technologies are **important because proprietary solutions fragment the industry**. Standards are particularly **important** when there is a **need to physically/logically connect entities** through an interface.
- IoT **standardization spans many domains**, including physical interfaces, access connectivity, networking and applications.
- Some **special considerations** need to be taken when designing standards for the IoT, including scalability, power efficiency, security and privacy.
- To make the IoT a practical reality, significant **research is required** in these technological areas.
- Some **areas of active research** include:
  - Standardization at all layers.
  - Architectures and middleware for IoT integration.
  - Lightweight implementations of cryptographic stacks.
  - Routing algorithms for the IoT.

### IoT Definitions

#### Internet of Things

A broadly-deployed aggregate computing/communication application and/or application-consumption system, that is deployed over a local (L-IoT), metropolitan (M-IoT), regional (R-IoT), national (N-IoT), or global (G-IoT) geography, consisting of

1. dispersed instrumented objects (“things”) with embedded one or two-way communications and some (or, at times, no) computing capabilities,
2. where objects are reachable over a variety of wireless or wired local area and/or wide area networks, and,
3. whose inbound data and/or outbound commands are pipelined to or issued by a(n application) system with a (high) degree of (human or computer-based) intelligence.

#### Sensors

- Sensors are active devices that measure some variable of the natural or man-made environment (e.g., a building, an assembly line, an industrial assemblage supporting a process).
- The technology for sensing and control includes electric and magnetic field sensors, optical and infrared sensors, radars, lasers, location/navigation sensors, etc.

#### Actuators

- An actuator is a mechanized device that accomplishes a specified physical action, for example, controlling a mechanism or system, opening or closing a valve, starting some kind or rotary or linear motion, or initiating physical locomotion. An actuator is the mechanism by which an entity acts upon an environment.
- The actuator embodies a source of energy, such as an electric current, and a source of physical interaction such as a hydraulic fluid pressure. It converts that energy into some kind of action or motion upon receipt of an external command or stimulus.

### IoT Frameworks (should we draw the diagram?)

- The IoT framework is in the form of a high level M2M system Architecture (HLSA).
- The HLSA is made of:
  - The **device and gateway domain**
  - The **network domain**
  - The **applications domain**
- The **device and gateway domain** consists of:
  1. **M2M Device**: A device that runs M2M applications using M2M service capabilities.
  2. **M2M area network**: Provides connectivity between M2M devices and M2M gateways. E.g. Personal Area Networks like Zigbee, Bluetooth, etc.
  3. **M2M Gateway**: A gateway that runs M2M applications using M2M service capabilities. Acts as a proxy between M2M devices and the network domain.
- The **network domain** consists of:
  1. **Access network**: A network that allows M2M devices and the gateway domain to communicate with the core network.
  2. **Core Network (CoN)**: A network that provides the following capabilities:
     - IP connectivity
     - Service and network control functions
     - Interconnection with other networks
  3. **M2M service capabilities**:
     - Provide M2M functions that are to be shared by different applications.
     - Expose functions through a set of open interfaces.
- The **applications domain** is composed of:
  1. **M2M applications**: Applications that run the service logic and use M2M service capabilities.
- There are also management functions within an overall M2M service provider domain:
  1. **Network management functions**: Consists of all the functions required to manage the access and core networks.
  2. **M2M management functions**: Consists of all the functions required to manage the M2M service capabilities.

### Basic Nodal Capabilities

- A remote device generally needs to have a **basic protocol stack** that supports at least **local connectivity** and **networking connectivity**. Additionally, some higher level application support protocols are generally needed.
- Typical requirements include:
  - **Retransmission**: Network recovers immediately from packet loss and informs the application.
  - The network is **independent of MAC/PHY**.
  - **Scale**: Supports thousands of nodes and multiple link speeds.
  - **Emergency messages** are routed and/or queued around other traffic.
  - Paradigm supports **peer-to-peer**. Not everything is client-server.
  - Network and application **versioning**.
  - Simple **publish/subscribe** parsers.
  - **Security**: Supports strong encryption, mutual authentication, Suite B ciphers and protects against record/playback attacks.