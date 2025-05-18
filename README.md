# Atlas

This Project was done as part of our Product Design Studio module at Singapore University of Design and Technology, partnering with Nika Planet.
 
Atlas is an innovative hybrid VTOL drone solution engineered to overcome real-world constraints in geospatial mapping missions. Designed for vertical takeoff and fixed-wing cruise, Atlas eliminates the need for traditional runway space while enhancing flight efficiency and data acquisition. With a focus on modularity, endurance, and adaptability, Atlas streamlines operations in constrained environments—empowering teams with a smarter, more flexible approach to aerial intelligence.

### Problem Statement
How might we increase flight duration, while ensuring ease of launching and landing as well as portability for efficient geospatial data collection?

- VTOL drones are able to take off and land within constrained spaces but have low flight endurance
- fixed-wing drones are able to sustain longer flights but require a runway

In order to address these problems, we came up with Atlas as a solution.

*3D Visualised Render of Atlas*

![untitled 23](https://github.com/user-attachments/assets/df553a92-c5a9-4a03-bbbb-38029ef43181)

*Our Prototype*

![Prototype](https://github.com/user-attachments/assets/d30bc3a7-7352-48a3-ae61-018bb654b4e0)


## Project Done By:
- Aderic Choo
- Amit Sanke
- Isaac Oh - https://github.com/Isaac8116
- Jatlyson Ang  - https://github.com/jatlys
- Rittambhra Rani - https://github.com/ritzbizkit
![Group Picture](https://github.com/user-attachments/assets/70ee26fb-c722-4344-987c-58640c57cf4e)

### Hardware Components:
- Flight Controller: MATEK Mateksys F405-VTOL
- Electronic Speed Controller (ESC): LUCID 60a 4in1 ESC
- GPS:  MATEK Mateksys GNSS & Compass M10Q-5883
- Airspeed Sensor: MATEKSYS DIGITAL AIRSPEED SENSOR AS-DLVR-I2C
- Telemetry Radio: HolyBro SiK Telemetry Radio V3 
- VTOL Motors: T-Motor F60 Pro IV V2.0 1750KV
- Rear Motors: T-MOTOR AT2317 1400KV

## Prototype Videos

## HuskyLens Vision-Based AprilTag Detection
YouTube Video Link: https://youtu.be/luibbBOE88s 

### Overview
This section presents a proof-of-concept system for visual target detection using the HuskyLens AI camera. It is part of a larger effort to develop an autonomous landing and navigation pipeline for drones. In this setup, a Raspberry Pi 3B communicates with the HuskyLens via UART and forwards parsed detection data as MAVLink messages to a flight controller. This serves as an initial prototype for what will later be transitioned to a wireless MAVLink telemetry-based architecture in final deployment.

### System Architecture
- HuskyLens Camera: Performs onboard tag detection and tracking. Sends data over UART.
- Raspberry Pi 3B: Acts as the intermediary processing unit. It receives serial input from HuskyLens, extracts relevant information (e.g., tag ID, position), and constructs corresponding MAVLink messages.
- Flight Controller: Receives MAVLink LANDING_TARGET and HEARTBEAT messages from the Raspberry Pi via USB or telemetry port.
- Ground Control Station: Displays received data in software such as Mission Planner for debugging and demonstration purposes.

### Proof-of-Concept Objectives
- Demonstrate basic communication between the HuskyLens and Raspberry Pi using UART.
- Parse detection output and reformat it into MAVLink-compatible messages.
- Transmit LANDING_TARGET messages to simulate visual target tracking.
- Maintain a HEARTBEAT connection with the ground station to simulate real-time system activity.
- Provide a working baseline for transitioning to wireless telemetry in future iterations.

### Future Development
- Replace UART with wireless MAVLink telemetry for long-range, real-time communication.
- Integrate a Livox or similar high-resolution depth camera to improve detection fidelity.
- Implement GPS-based coordination and landing logic in flight controller firmware.
- Develop a modular interface for switching between multiple sensor input sources.
- Optional migration to ROS2 for more complex system orchestration if needed.

## Poster
![A1 Poster](https://github.com/user-attachments/assets/a028dfdb-560e-428b-bd2b-a76988331b78)

