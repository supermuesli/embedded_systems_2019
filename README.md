# embedded_systems_2019
Markdown of Embedded Systems 2019 @ RWTH Aachen University

---

# Embedded and embedding Systems
- *embedded systems* are modular devices that complete specific tasks in realtime
- **typical functionalities**:
  - measuring physical variables (sensing)
  - influencing physical variables (acuating)
  - storing/monitoring data
- **important disciplines**:
  - signal processing
  - control engineering
  - measurement/sensor technology
- as an example, the camera module is an embedded system in your cellphone (the embedding system) 
- **we categorize embedded systems into *product automation* and *production automation***

|                | Device Technology | Programming Languages | Examples |
|----------------|-------------------|-----------------------|----------|
| **Product**    | **Microcontrollers**, **Programmable Hardware**, Digital Signal Processors | C, Assembler, MATLAB/Simulink, Java | Car electronics |
| **Production** | **Programmable Logic Controllers (PLC)**, Distributed Control Systems (DCS), Industrial PCs (IPC) | IL, LD/RLL, FBD, SFC, CFC | Manufacturing Control, Logistics, Chemical Process Control |


- **similarities** in *product* and *production* automation:
  - requirements for embedded system must be derived from requirements for embedding system
  - strong realtime, safety, reliability, maintainability and evolvability requirements
  - rising complexity and quality concerns
- **differences** in *product* and *production* automation:
  - mass production vs unique & custom-made plants
  - resource constraints (for product automation systems: weight, cost, energy consumption, mounting space)
  - relationship between manufacturer, supplier, operator and user
  - operation and maintenance
  - device technologies and programming languages

# Microcontrollers
- *microcontrollers* are stand-alone devices for embedded applications
- often made up of **microprocessor + memory + I/O + additional peripherals**
- **only complete specific tasks**
- **microcontrollers with the same microprocessor are considered to be in the same family**
- **Peripherals:**
  - a peripheral is a hardware/device with input/output interfaces
  - common peripherals are keyboards, speakers, headsets, ...
- **Digital I/O:**
  - we can access external hardware via digital I/O pins
  - ports are made up of n pins on an n-bit architecture
  - available registers are: PIN (Port Input Register), PORT (Port Register), DDR (Data Direction Register)
  - PIN:
    - read only
    - contains high or low bits of all pins
    - usually used for reading input pins
  - PORT:
    - read/write
    - specifies the output bits
    - some ATMega microcontrollers use this register for activating Pull-Up resistors for input pins
  - DDR:
    - read/write
    - specify data direction of each pin of a port
- **Timers, Counters, PWM:**
- **DA/AD Conversion:**
  - Digital/Analog Conversion: PWM, 
  - Analog/Digital Conversion: SAR-Network

# Data buses
- **Topologies:**
- **Physical layer - problems and solutions:**
- **Data link layer (Logic link control and medium access controll):**
- **I²C, CAN, FlexRay, Profibus:**

# Programmable logic controllers
- **Discrete controls:**
- **Languages:**
- **Standard function blocks:**

# Real time
- **Hard/soft realtime:**
- **Deadlocks:**
- **Priority inversion and how to avoid it:**
- **Sporadic and periodic scheduling:**

# Embedded software design
- **Development process models:**
- **Functional requirements:**
- **Quality requirements:**
- **Architecture:**

# Softwaredevelopment with Simulink
- **MATLAB/Simulink:**
- **Subsystems:**
- **Buses:**
- **Embdedded code generation:**
- **Model-based testing:**
