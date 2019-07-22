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
  - common peripherals: keyboard, speaker, USB-Port, Audio/Headphone-Jack, HDMI-Interface, ...
- **Digital I/O:**
  - we can access or monitor external hardware via digital I/O pins
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
  - **Problems with Digital Input**:
    - signal does not always have a well-defined level
    - signal noise
    - signal bouncing
  - **Solutions**:
    - schmitt-trigger
    - low-pass-filter
    - noise-cancellation
    - sampling the input multiple times
- **Timers, Counters, PWM:**
  - interrupt: interrupt service routine is executed if specific interrupt occured
  - polling: periodically check for state-change and act accordingly
  - counter:
    - counts external events
    - for example number of rising edges on PIN2
  - timer:
    - is basically a counter
    - counts number of clock cycles (with or without prescaler)
  - timers/counters have a counter-register which can be incremented or decremented
  - important flags for timers/counters are: start/stop-flag, interrupt-enable/disable flag, prescaler and mode of operation
  - other features of timers/counters: input capture, output compare, pulse width modulation 
- **DA/AD Conversion:**
  - Digital/Analog Conversion: PWM, R2R-Network
  - Analog/Digital Conversion: SAR-Network, Tracking-Converter, Flash-Converter

# Data buses
- **Topologies:**
  - **bus:**
    - only one partner can send at a time
    - cheap
    - collisions can occur
  - **star:** 
    - multiple partners can send at the same time
    - expensive and more wiring required
  - **ring:**
    - high quality of service
    - no multiple access
    - complex
- **Physical layer:**
  - defines how bit streams are transported
  - mechanical and electrical characteristics
  - bit encoding
  - synchronization
- **Data link layer (Logic link control and medium access controll):**
  - defines how messages are transported
  - frame formats
  - medium access
  - error correction and flow control
  - **medium acces controls (MAC):**
    - CSMA/CR (collision resolution)
    - CSMA/CD (collision detection)
    - master-slave
    - aloha
- **I²C, CAN, FlexRay, Profibus:**
  - **I²C (Inter integrated circuit):**
    - intra board communication
  - **CAN (Controller Area Network):**
    - intra car communication
  - **FlexRay:**
    - intra car communication with real time and higher data rates
  - **Process Field Bus(PROFIBUS):**
    - industrial controllers
# Programmable logic controllers
- supposed to monitor and plot variables
- variables can be plotted as they come (continuous) or in classified form (discrete)
- **Languages:**
  - function block diagramm (FBD)
  - ladder diagram (LD)
  - instruction list (IL)

# Real time
- **Hard/soft realtime:**
  - hard realtime: task is always completed under given threshold amount of time
  - soft realtime: task is on average completed under given threshold amount of time
  - a watchdog can help meeting the time threshold constraint
- **Deadlocks:**
  - classic deadlock:
    - process A holds resource R1 and needs resource R2
    - process A is preempted process B
    - process B holds resource R2 and needs resource R1
    - oh fuck
  - priority inversion:
    - process A has high priority and need resource R
    - process B has ulrta low priority and currently holds resource R
    - oh fuck
    - fix like this: let B inherit the priority of A and let B be non-preemptable by processes with lower priority
- **Sporadic and periodic scheduling:**
  - 

# Embedded software design
- **Development process models:**
  - waterfall
  - spiral
  - extreme programming
  - v-modell
- **Functional requirements:**
  - what it does
- **Quality requirements:**
  - how good it does it:
    - **system cost**
    - **power consumption**
    - **mounting space**
    - dependability
    - modifiability
    - integrability
    - reusability
    - testability
    - performance
    - decomposability
    - marketability
    - system qualities
- **Architecture:**
  - defines constraints on the implementation
  - dictates organizational structure
  - inhibits or enables a systems quality
  - it is possible to predict system quality by studying the architecture

# Softwaredevelopment with Simulink
- **MATLAB/Simulink:**
- **Subsystems:**
- **Buses:**
- **Embdedded code generation:**
- **Model-based testing:**
