# Week 12 - Internet of Things (IoT) & Cloud Computing

## 1. Introduction to Smart Cities
- **What is a Smart City?**
  - A **Smart City** uses IoT technology to improve sustainability, productivity, and livability.
  - Smart cities integrate digital infrastructure, like sensors and data analytics, to optimize city resources and services.

- **Smart City Projects**:
  - **Ipswich, Australia**: A leader in smart city initiatives, featuring projects like:
    - **Smart Waste**: Sensors detect when bins are full, optimizing collection routes.
    - **Smart Lighting**: Adjusts street lighting based on time and weather.
    - **Smart Parking**: Monitors parking availability to guide drivers to open spots.
    - **Environmental Sensing**: Tracks air quality and weather conditions.
  - **SMIGHT Base**: Combines public Wi-Fi, emergency calls, environmental sensors, and charging points, all integrated into street lighting.

---

## 2. Internet of Things (IoT)
- **What is IoT?**
  - **Internet of Things (IoT)** connects everyday devices to the internet, allowing them to send and receive data.
  - IoT enables devices like smart thermostats, sensors, and wearable tech to share data and interact intelligently.

- **IoT Applications**:
  - **Smart Homes**: Thermostats, lights, and security systems controlled remotely.
  - **Healthcare**: Wearable health devices that monitor heart rate, glucose levels, etc.
  - **Agriculture**: Soil and weather sensors optimize crop growth.

- **Communication Technologies in IoT**:
  - **Long-Range**:
    - **LoRa (Long Range)**: Ideal for rural areas, supports 20-30 km ranges in open fields.
    - **SigFox**: Offers long-distance coverage but limited data transfer (small MTU size).
    - **LTE-M and NB-IoT**: Licensed bands with higher data rates, used for IoT in cellular networks.
  - **Short-Range**:
    - **Wi-Fi**: High data rates over short distances (100-250 m).
    - **Bluetooth**: Common for personal area networks (PANs).
    - **Zigbee**: Low-power, short-range communication used in home automation.

---

## 3. IoT Ecosystem and Architectures
- **Components of IoT**:
  - **End Devices**: Sensors or actuators that collect or respond to data (e.g., temperature sensors).
  - **Gateways**: Devices that manage data flow between IoT devices and the internet.
  - **Cloud Storage**: Stores and processes data from IoT devices.

- **IoT Architecture**:
  - **Horizontal Structure**:
    - **IoT Sensor Network**: Collects data from sensors.
    - **Edge Network**: Handles initial data processing close to the source.
    - **Backend Network**: Stores data in the cloud for further processing and analysis.
  - **Vertical Structure**:
    - **Application Layer**: Includes software and apps users interact with.
    - **Network Layer**: Connects devices, sensors, and gateways.
    - **Physical Layer**: Consists of physical IoT devices and sensors.

---

## 4. IoT Network Design and Management
- **IoT Network Setup**:
  - **Network Design**: Involves hardware selection, protocol selection, and gateway placement.
  - **Power Management**: Essential for low-power IoT devices, ensuring long battery life.
  - **Security**: Protects IoT networks from unauthorized access and attacks.
  - **Scalability**: Supports the addition of more devices as the network grows.

- **IoT Security Challenges**:
  - **Limited Security**: Many IoT devices lack strong security, making them vulnerable.
  - **Replay Attacks**: Attackers can capture data and re-send it, potentially causing unwanted actions (e.g., turning devices on/off).

---

## 5. Skills for IoT Jobs
- **Hardware Skills**: Knowledge of microcontrollers like Arduino, STM32, or ESP32.
- **Networking and Protocols**: Understanding communication protocols (e.g., Wi-Fi, LoRa).
- **Programming**: Skills in C/C++ or Python for IoT device programming.
- **Data Analytics**: Analyzing data from IoT devices to derive useful insights.

---

## 6. Introduction to Cloud Computing
- **What is Cloud Computing?**
  - Cloud computing provides on-demand access to a shared pool of configurable computing resources, such as servers, storage, and applications, over the internet.
  - Cloud resources can be scaled up or down based on user needs, offering flexibility and cost savings.

- **Benefits of Cloud Computing**:
  - **Reduced IT Costs**: Reduces the need for on-premises hardware and IT maintenance.
  - **Scalability**: Allows resources to be scaled based on demand.
  - **Business Continuity**: Data is stored in the cloud, reducing downtime risks from natural disasters or power failures.
  - **Flexibility**: Users can access data and applications from anywhere with internet access.

---

## 7. Cloud Service Models
- **Infrastructure as a Service (IaaS)**:
  - Provides virtualized computing resources over the internet, such as virtual servers and storage.
  - **Examples**: Google Cloud Storage, Amazon EC2.
  - **Benefits**: Users manage their applications and operating systems, while the provider manages the infrastructure.

- **Platform as a Service (PaaS)**:
  - Provides a platform allowing users to develop, run, and manage applications without the complexity of building and maintaining the infrastructure.
  - **Example**: Microsoft Azure.
  - **Benefits**: Supports application development and testing, simplifying deployment processes.

- **Software as a Service (SaaS)**:
  - Delivers applications over the internet as a service, eliminating the need for installation and maintenance.
  - **Examples**: Google Workspace, Microsoft Office 365.
  - **Benefits**: Users can access software through a web browser, while the provider handles updates and maintenance.

---

## 8. Risks and Challenges of Cloud Computing
- **Vendor Lock-In**:
  - Switching providers can be difficult due to incompatibilities in cloud systems.
  - **Example**: Moving data from Amazon Web Services (AWS) to Microsoft Azure may require modifications to applications.

- **Service Availability**:
  - Cloud providers may experience downtime, affecting service availability for clients.
  - Users must evaluate the provider’s reliability and backup strategies.

- **Data Security and Privacy**:
  - Data stored in the cloud is vulnerable to unauthorized access, making encryption and access controls essential.
  - **Legal Ownership**: Users should clarify who owns the data stored in the cloud to avoid conflicts.

---

## Summary
- IoT enables smart city solutions, enhancing efficiency and livability through connected devices.
- Cloud computing provides scalable, on-demand resources, offering three primary service models: IaaS, PaaS, and SaaS.
- Both IoT and cloud computing present new challenges in security and management, highlighting the need for proper network design, data protection, and skilled personnel.

---

