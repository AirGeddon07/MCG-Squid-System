Magnetocardiography (MCG) SQUID System

<img width="1344" height="768" alt="mcg_squid_system_VISUAL" src="https://github.com/user-attachments/assets/e607d359-72e2-4887-b26a-9df906c74e89" />
This project implements a portable Magnetocardiography (MCG) system using a multi-channel low-temperature SQUID (Superconducting QUantum Interference Device) sensor array. The system measures the extremely weak magnetic fields produced by cardiac electrical activity. Key features include a cryogenic SQUID sensor housed in a lightweight carbon-fiber cryostat, a robotic gantry for sensor positioning, ultra-low-noise analog front-end electronics (preamplifiers, filters, lock-in amplifiers), high-resolution ADC and FPGA processing, and an embedded AI computer for control and data analysis. A battery-powered design with wireless connectivity enables untethered operation. This README documents the hardware components, assembly steps, wiring connections, software setup, and usage examples for building and using the MCG SQUID system.

<img width="1243" height="864" alt="MCG visual 2" src="https://github.com/user-attachments/assets/4e773ef3-8f1b-4238-be81-b50a1e5d8170" />

For Detailed Blueprint Check out : 
https://www.blueprint.am/s/-HDn8-X4wVu4Uc4gdqizYnHnoETic48dUwH4BOvl_gQ 

Key Components
The main components of the MCG system (as listed in the BOM) are:

SQUID Sensor Array (Multi-Channel Low-Tc SQUID) –

<img width="500" height="461" alt="image" src="https://github.com/user-attachments/assets/de7c7fc6-8202-403d-9f3e-e9829ab4d509" />

A superconducting magnetic sensor array that detects pico- to femto-Tesla magnetic fields
. The low-Tc SQUID requires cryogenic cooling (typically ~4 K) to operate.

Estimate: 1 × $250000.00 = $250000.00

Sourcing Options:

https://www.digikey.com/search/en?q=SQUID%20sensor
https://www.mouser.com/Search/Refine?Keyword=SQUID+sensor
https://www.ptb.de/cms/en/ptb/research-development/8-divisions/82-quantum-metrology/822-quantum-magnetometry/8221-squid-metrology.html

Description:
Superconducting Quantum Interference Device array for detecting ultra-weak magnetic fields. Requires cryogenic cooling.

Technical Specifications

A Multi-Channel Low-Tc SQUID is a highly sensitive sensor array engineered for the detection of extremely weak magnetic fields, leveraging superconducting quantum interference device technology. This device requires cryogenic cooling to maintain its superconducting state, enabling ultra-low noise measurements. It provides multiple analog output channels for precise, real-time magnetic field data acquisition.

Measurement Range: 1 femtotesla (fT) to 10 picotesla (pT)

Accuracy/Precision: Femtotesla-level (fT) precision

Resolution: Sub-femtoTesla (fT)

Output Interface: Multi-channel Analog Voltage Output

Operating Voltage: Typically 3.3V - 5V DC (for bias and feedback electronics)

Response Time: Microseconds (µs)

Power Consumption: Low milliwatts (mW) for SQUID bias and readout electronics (excluding cryocooler)

Pins:
Analog Output Channels

Bias Input

Feedback Input

Physical / Print
Dimensions: 200x200x150mm (sensor head)

Connections:

<img width="1485" height="483" alt="image" src="https://github.com/user-attachments/assets/6372ea62-a2fb-439a-9c7f-90111dd2f5d1" />

Cryogenic Cooler (Closed-Cycle GM Cryocooler) – 

<img width="500" height="281" alt="image" src="https://github.com/user-attachments/assets/a796c5d8-5908-4d2b-a38c-5a4a3f726941" />

A Gifford-McMahon closed-cycle refrigerator that provides the necessary cryogenic temperature for the SQUID. It is integrated into the carbon-fiber cryostat housing.
Analog Signal Chain

Estimate: 1 × $75000.00 = $75000.00

Sourcing Options:

https://www.arscryo.com/cryocooler-principles-of-operation
https://bluefors.com/products/gifford-mcmahon-cryocoolers/
https://shicryogenics.com/products/cryocoolers/
https://www.digikey.com/search/en?q=Gifford-McMahon%20Cryocooler
https://www.mouser.com/search/refine?q=Gifford-McMahon%20Cryocooler

Description
Provides the necessary cryogenic temperatures for SQUID sensor operation without liquid helium.

Technical Specifications:

The Closed-Cycle Gifford-McMahon Cryocooler is an essential component for achieving and maintaining cryogenic temperatures without the need for liquid helium. It operates by a thermodynamic cycle using a regenerator and a displacer to cool the cold head. Crucially, it provides the stable ultra-low temperatures required for the sensitive operation of SQUID sensors, making it a critical part of the MCG SQUID System.

Minimum Temperature (Typical range): 3.5K to 10K (first stage often 50-80K)

Cooling Capacity (Typical range): 0.5W to 2W at 4.2K (often higher at higher temperatures like 77K on first stage)

Operating Voltage: 240VAC

Power Consumption (Typical range): 1.5kW to 5kW during operation (compressor unit)

Cool-down Time (Typical range): 2 to 4 hours to reach base temperature

Weight (Typical range): 30kg to 100kg (cold head and compressor combined)

Vibration Level: 
Can produce vibrations; specific models designed for low vibration are critical for SQUID applications

Noise Level:
Compressor unit can be noisy (50-70 dBA); cold head is quieter

Pins:
240VAC Input
Control Signals

Physical / Print
Dimensions: 400x300x300mm

Connections:

<img width="1138" height="559" alt="image" src="https://github.com/user-attachments/assets/0074b432-8271-40e0-af5d-04bd282c78d0" />

Low-Noise Pre-Amplifier Array (e.g. ADA4807-4) – 

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/c22395c4-0594-4afd-87fa-6eb1637adf8f" />

Custom analog amplifier boards to boost the tiny SQUID output signals with minimal added noise. Typical devices like the ADA4807 offer ~3.1 nV/√Hz noise density

Estimate: 1 × $800.00 = $800.00

Sourcing Options:

https://www.digikey.com/en/products/detail/analog-devices-inc/ADA4807-4ARUZ-EBZ/5583160
https://www.digikey.com/en/products/detail/analog-devices-inc/AMC-ADA4807-2ARMZ/9916377
https://www.mouser.com/Search/Refine?N=13063853&Keyword=ADA4807+Quad+Module

Description:
Amplifies extremely weak SQUID signals with minimal added noise before further processing.

Technical Specifications:

The Analog Devices ADA4807 Quad Pre-Amp Module is a high-speed, low-noise operational amplifier designed to amplify extremely weak analog signals, such as those from SQUID sensors. Its wide 1 GHz bandwidth and low input voltage noise make it ideal for sensitive scientific instrumentation requiring minimal signal degradation. Operating typically on +/-5V supplies, it provides four independent amplification channels for multi-sensor applications.

Operating Voltage: +/-5V DC

Power Consumption (Quiescent): ~20.8 mA (total for quad)

Bandwidth (-3dB): 1 GHz

Input Voltage Noise: 0.94 nV/√Hz

Slew Rate: 390 V/µs

Number of Channels: Quad (4)

Communication Protocol: Analog Signal Path

Data Rate: N/A (Analog Bandwidth: 1 GHz)

Range: Output Voltage Swing (e.g., +/-3.8V @ +/-5V supplies)

Antenna Type: N/A

Supported Standards/Versions: N/A

Pins:

Analog Inputs (xN)

Analog Outputs (xN)

+/-5V Power: Ground

Physical / Print

Dimensions: 100x60x10mm

Connections:

<img width="1479" height="679" alt="image" src="https://github.com/user-attachments/assets/f00442f5-4cb1-4e36-b7df-f73405021a85" />

RF Filter Array – 

<img width="500" height="379" alt="image" src="https://github.com/user-attachments/assets/2e2d768a-6806-4882-bdc8-f31e56970b63" />

EMI filter board that removes high-frequency interference before lock-in detection.

Estimate: 1 × $300.00 = $300.00

Sourcing Options:

https://www.sparkfun.com/custom_circuit_boards
https://www.digikey.com/en/products/filter/emi-rfi-filters-lc-rc-networks/835
https://www.digikey.com/en/products/filter/emi-filter-kits/646

Description:
Passively filters out high-frequency electromagnetic interference before signal amplification.

Technical Specifications:

The Custom EMI Filter Board is a crucial passive electrical module designed to remove high-frequency electromagnetic interference from signals. It ensures signal integrity before amplification by blocking unwanted noise that could degrade performance. This board is essential for maintaining clean signal paths in sensitive instrumentation like the MCG SQUID System.

Frequency Range: 100 kHz - 1 GHz (typical for high-frequency EMI)

Attenuation: >40 dB at target frequencies

Input/Output Impedance: 50 Ohm (matched to signal path)

Maximum Operating Voltage: ±15 V (common for analog signal paths)

Maximum Current Rating: 100 mA per channel

Number of Channels: Configurable based on input/output pins

Power Consumption: Negligible (passive component)

Communication Protocol: Not Applicable (passive analog filter)

Data Rate: Not Applicable (processes analog signals)

Range: Not Applicable (no communication range)

Antenna Type: Not Applicable (not an RF transceiver)

Supported Standards/Versions: Not Applicable (no communication standards)

Pins:

Input Channels

Output Channels

Ground

Physical / Print
Dimensions: 80x50x8mm

Connections:

<img width="1081" height="587" alt="image" src="https://github.com/user-attachments/assets/04d727ab-8be5-4397-b419-22f6d2365cba" />

Multi-Channel Lock-In Amplifier (e.g. Zurich Instruments MFLI) –

<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/e0d77704-000b-4948-a22c-ec47e2ee2e15" />

Demodulates and extracts the signal of interest from the noisy background by phase-sensitive detection.

Estimate: 1 × $35000.00 = $35000.00

Sourcing Options:

https://www.ebay.com/itm/205640593767
https://www.digikey.com/search/en?q=Zurich%20Instruments%20MFLI
https://www.mouser.com/search/?q=Zurich%20Instruments%20MFLI

Description:
Extracts small signals from noisy backgrounds using phase-sensitive detection. High-speed multi-channel operation.

Technical Specifications:

The Zurich Instruments MFLI Lock-in Amplifier is a high-performance instrument designed for extracting small AC signals from noisy backgrounds using phase-sensitive detection. It offers a wide frequency range and excellent dynamic reserve, making it suitable for demanding applications in various fields. Connectivity via USB and Gigabit Ethernet, coupled with comprehensive API support, ensures flexible integration into complex experimental setups.

Frequency Range: DC to 500 kHz or 5 MHz (model dependent)

Demodulation Bandwidth: Up to 1 MHz

Input Noise Density: < 2.5 nV/√Hz

Dynamic Reserve: > 120 dB

Communication Protocol: USB 2.0, Gigabit Ethernet

Operating Voltage: 100-240 VAC, 50/60 Hz

Power Consumption: < 50 W

API Support: LabVIEW, MATLAB, Python, C

Pins:

Signal Inputs

Reference Input

Demodulated Outputs

USB

Ethernet

Physical / Print
Dimensions: 450x300x150mm

Connections:

<img width="1141" height="609" alt="image" src="https://github.com/user-attachments/assets/6d49ac8e-5f29-45d8-b256-41eacca9fb37" />

High-Resolution ADC Module (e.g. AD7768) –

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/6dae3eff-2b69-432f-9c1c-86b824a97632" />

A 24-bit analog-to-digital converter that digitizes the lock-in outputs. The AD7768-1 evaluation board provides multiple ADC channels and digital interfaces.
Digital Processing

Estimate: 1 × $500.00 = $500.00

Sourcing Options:

https://www.digikey.com/en/products/detail/analog-devices-inc/EV-AD7768-1FMCZ/9370883
https://www.mouser.com/Search/Refine?Keyword=EV-AD7768-1FMCZ
https://www.analog.com/en/resources/evaluation-hardware-and-software/evaluation-boards-kits/eval-ad7768-1.html

Description:
Converts analog signals from the lock-in amplifier into high-resolution digital data.

Technical Specifications:

The Analog Devices AD7768-1 Evaluation Board serves as a high-resolution, 24-bit, 256 kSPS ADC module designed to convert analog signals into precise digital data. It utilizes an SPI interface for data output and features flexible analog input configuration. This board is crucial for applications requiring accurate digitization of low-frequency analog signals, such as those from a lock-in amplifier in a SQUID system.

Communication Protocol: SPI (Serial Peripheral Interface)

Data Rate: Up to 256 kSPS (kilo-samples per second)

Resolution: 24-bit

Input Voltage Range: Configurable, typically differential up to +/-2.5V or 5V single-ended

Operating Voltage: Typically 5V DC power input (board), with internal regulation for ADC supplies

Power Consumption: Approximately 100 mW (typical for the AD7768-1 chip)

Antenna Type: Not applicable (ADC module)

Supported Standards/Versions: Sigma-Delta ADC Architecture

Pins:

Analog Inputs

SPI Data Out

Clock

CS

Power Input

Physical / Print
Dimensions: 100x70x12mm

Connections:

<img width="1588" height="748" alt="image" src="https://github.com/user-attachments/assets/bbcb09ea-dc7d-4669-9d35-f621bc16c2dd" />

FPGA/DSP Processor (Xilinx Zynq-7000 SoC) –

<img width="500" height="498" alt="image" src="https://github.com/user-attachments/assets/83c6c86a-d857-4887-94fa-0bd84d91c016" />

A reprogrammable logic board that handles real-time signal processing and data aggregation. Communicates with the ADC over SPI and with the embedded computer over PCIe.

Estimate: 1 × $1200.00 = $1200.00

Sourcing Options:

https://www.digikey.com/en/products/detail/xilinx-inc/XC7Z035-L2FBG676I/XC7Z035-L2FBG676I-ND/5247378
https://digilent.com/shop/zybo-z7-zynq-7000-arm-fpga-soc-development-board/
https://www.mouser.com/Search/Refine?Keyword=Xilinx+Zynq-7000+SoC+Module

Description:
Performs real-time signal conditioning, initial noise reduction, and high-speed data buffering before AI processing.

Technical Specifications:

The Xilinx Zynq-7000 SoC Module integrates a dual-core ARM Cortex-A9 processor with Xilinx 7 series programmable logic (FPGA) on a single die, providing a powerful platform for real-time processing and hardware acceleration. It is ideal for applications requiring high-speed data buffering, custom signal conditioning, and intelligent pre-processing before more complex AI tasks, leveraging its heterogeneous architecture for optimal performance in embedded systems.

Processor Core: Dual-core ARM Cortex-A9 MPCore

Processor Clock Speed: Up to 1 GHz

Programmable Logic (FPGA): Artix-7 or Kintex-7 equivalent logic cells (varies by model)

DDR Memory Interface: Supports DDR3 (DDR4 on specific modules)

On-chip Memory: Up to 512 KB OCM (On-Chip Memory) and Block RAM in PL

Operating Voltage (Core): 0.9V - 1.0V (various I/O voltages)

Built-in Peripherals (PS): 2x UART, 2x SPI, 2x I2C, 2x CAN, USB 2.0, Gigabit Ethernet

Analog-to-Digital Converter: Integrated XADC block in PL (up to 1 MSPS, 12-bit)

GPIO Pins: Highly configurable via PS and PL (typically 100+ user I/Os)

Pins:

SPI Input

PCIe Output

DDR4 RAM

GPIOs

Power Input

Physical / Print
Dimensions: 100x80x15mm

Connections:

<img width="1094" height="625" alt="image" src="https://github.com/user-attachments/assets/0d0cdd28-a1f7-4752-9359-47cf08004db4" />

Embedded AI System (NVIDIA Jetson AGX Xavier NX) – 

<img width="500" height="189" alt="image" src="https://github.com/user-attachments/assets/eec814a7-4529-482e-adc0-7aa8231180eb" />

A compact AI supercomputer (up to 21 TOPS) that runs high-level control software and machine learning models. It interfaces with the FPGA (PCIe), wireless module, and motor controller.

Estimate: 1 × $600.00 = $600.00

Sourcing Options:

https://www.digikey.com/en/products/detail/seeed-technology-co-ltd/102110427/12323559
https://www.generationrobots.com/en/403635-nvidia-jetson-xavier-nx-developer-kit.html
https://developer.nvidia.com/buy-jetson

Description:
Powerful embedded platform for running AI inference models to filter EMI and localize magnetic fields.

Technical Specifications:

The NVIDIA Jetson Xavier NX is a compact yet powerful embedded AI computing platform, designed for deploying high-performance AI inference at the edge. It combines a 6-core ARM CPU and a Volta GPU with Tensor Cores, offering significant processing power for AI and machine learning applications. Its small form factor and multiple power modes make it suitable for power-constrained devices and systems requiring advanced compute capabilities.

CPU: 6-core NVIDIA Carmel ARMv8.2 CPU (up to 1.9 GHz)

GPU: 384-core NVIDIA Volta GPU with 48 Tensor Cores

AI Performance: 21 TOPS (INT8)

System Memory: 8 GB 128-bit LPDDR4x

Internal Storage: 16 GB eMMC 5.1

Power Modes: 10W / 15W / 20W

GPIO Pins: Up to 40 (via header)

Key Peripherals: PCIe Gen3, USB 3.1 Gen2, Gigabit Ethernet, MIPI CSI/DSI, UART/SPI/I2C

Pins:

PCIe Input

Ethernet

USB3.0

GPIO

Power Input

CSI/DSI

Physical / Print
Dimensions: 70x45x8mm

Connections:

<img width="987" height="552" alt="image" src="https://github.com/user-attachments/assets/a5a93d76-b70d-401f-baa8-278d2d6257b5" />

Wireless Communication Module (Intel AX210) – 

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/067f34f9-df75-4aec-b317-f46a30e452b2" />

A Wi-Fi 6E wireless card (M.2/PCIe form factor) providing high-bandwidth, low-latency data link to a remote control station.
Power Electronics

Estimate: 1 × $30.00 = $30.00

Sourcing Options:

https://www.amazon.com/OKN-AX210NGW-Bluetooth-Wireless-Ultra-Low/dp/B08MJLPZPL
https://www.digikey.com/en/products/search?keywords=Intel%20AX210%20WiFi%206E%20Module
https://www.mouser.com/c/embedded-solutions/wireless-connectivity/wi-fi-modules/?q=Intel%20AX210%20WiFi%206E%20Module

Description:
Provides high-bandwidth, low-latency wireless data transmission to a control station.

Technical Specifications:

The Intel AX210 WiFi 6E Module provides high-bandwidth, low-latency wireless data transmission using the latest Wi-Fi 6E (802.11ax) and Bluetooth 5.2 standards. It integrates via a PCIe interface, offering data rates up to 2.4 Gbps, making it ideal for robust wireless communication in demanding applications like the MCG SQUID System. This module requires external antennas for operation and typically runs on 3.3V.

Communication Protocol: Wi-Fi 6E (IEEE 802.11ax), Bluetooth 5.2

Data Rate: Up to 2.4 Gbps (Wi-Fi 6E, 160MHz channels)

Range: Environment dependent, typically up to 30m indoors

Operating Voltage: 3.3V (via M.2 interface)

Power Consumption: Typically 1-5W (varies with activity)

Antenna Type: External via MHF4 connectors

Supported Standards/Versions: IEEE 802.11ax (Wi-Fi 6E), 802.11a/b/g/n/ac/ax, Bluetooth 5.2

Pins:
PCIe Interface
Antenna Connectors
Power Input

Physical / Print
Dimensions: 22x30x2.4mm (M.2)

Connections:

<img width="908" height="321" alt="image" src="https://github.com/user-attachments/assets/66ea67d8-3de2-4d01-9d4d-5deba1d5f5ea" />

SQUID Cryogenic Power Supply (Keithley 2400 SourceMeter) –

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/e101d699-99d3-462a-83c8-4acf16a58475" />

Provides ultra-stable low-noise current and voltage bias to the SQUID array.

Estimate: 1 × $7000.00 = $7000.00

Sourcing Options:

https://www.mouser.com/ProductDetail/Keithley-Instruments-Inc/2400?qs=yBvC8ON7YZ3CxGCjcXlIIQ%3D%3D
https://www.transcat.com/keithley-2400-digital-sourcemeter
https://www.testequity.com/product/14592-4-2400

Description:
Provides ultra-stable, low-noise current and voltage to the SQUID sensors.

Technical Specifications:

The Keithley 2400 Series SourceMeter is a high-precision instrument capable of simultaneously sourcing and measuring voltage or current. It offers a wide dynamic range, high accuracy, and low noise performance crucial for sensitive applications like biasing SQUID sensors. Its versatility makes it an indispensable tool for characterization and test in various research and industrial settings.

Input Voltage Range: 100-240 VAC, 50/60 Hz

Output Voltage Range: ±5 µV to ±200 V (with various sub-ranges)

Maximum Current Source/Sink: ±10 nA to ±1 A (with various sub-ranges)

Maximum Output Power: 20 W

Voltage Programming Accuracy: 0.012% of reading + 0.005% of range

Current Programming Accuracy: 0.02% of reading + 0.005% of range

Voltage Noise (p-p, 0.1Hz to 10Hz): Typically <100 µV

Overload Protection: Voltage and current limit protection; thermal shutdown

Pins:

AC Input

SQUID Bias Output

Feedback Current Output

Physical / Print
Dimensions: 250x100x350mm

Connections:

<img width="746" height="378" alt="image" src="https://github.com/user-attachments/assets/92b1ce50-0086-43d6-a305-015922efa9fc" />

High-Capacity Battery Pack (LiFePO4 24V, 100Ah) –

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/488430c7-0d09-4253-acdb-ac98ad7e809c" />

Portable battery that supplies the entire system.

Estimate: 1 × $400.00 = $400.00

Sourcing Options:

https://www.digikey.com/en/products/filter/dc-dc-converters/922?s=N4IgTC5ODEsLxpBTAJgqgLgGIQMzBA
https://www.adafruit.com/category/139
https://www.mouser.com/c/power-supplies/dc-dc-converters/

Description:
Regulates and distributes power from the battery to various components (e.g., 24V, 12V, 5V, 3.3V rails).

Technical Specifications:

The Custom Multi-Output DC-DC Converter is a critical power management component for the MCG SQUID System, regulating and distributing power from the battery pack. It provides multiple stable voltage rails (24V, 12V, 5V, 3.3V) to various onboard components, ensuring reliable operation. Designed for high efficiency and low noise, it is essential for the sensitive instrumentation within the system.

Input Voltage Range: 20V - 30V DC (from High-Capacity Battery Pack)

Output Voltages: 24V, 12V, 5V, 3.3V DC

Maximum Current (24V Output): 5A

Maximum Current (12V Output): 8A

Maximum Current (5V Output): 10A

Maximum Current (3.3V Output): 5A

Efficiency: >90% (typical at full load)

Output Ripple & Noise: <20mVpp (24V, 12V), <10mVpp (5V, 3.3V)

Quiescent Current: <50mA (no load)

Thermal Shutdown: 160°C

Pins:

24V Input

24V Output

12V Output

5V Output

3.3V Output

Ground

Physical / Print
Dimensions: 150x100x25mm

Connections:

<img width="766" height="755" alt="image" src="https://github.com/user-attachments/assets/197a5b81-0358-4f6f-8218-39ceddd0d80a" />

Main Power Distribution Unit (Custom DC/DC Converter) – 

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/0d239793-60aa-44ff-943c-254f1f4110a5" />

Distributes power from the battery to all subsystems. Converts 24V to required voltages (240VAC for cryocooler, 19V for Jetson, 5V/12V for FPGA, 5V for ADC, etc.).
Motion & Structure

Estimate: 1 × $400.00 = $400.00

Sourcing Options:

https://www.digikey.com/en/products/filter/dc-dc-converters/922?s=N4IgTC5ODEsLxpBTAJgqgLgGIQMzBA
https://www.adafruit.com/category/139
https://www.mouser.com/c/power-supplies/dc-dc-converters/

Description:
Regulates and distributes power from the battery to various components (e.g., 24V, 12V, 5V, 3.3V rails).

Technical Specifications:

The Custom Multi-Output DC-DC Converter is a critical power management component for the MCG SQUID System, regulating and distributing power from the battery pack. It provides multiple stable voltage rails (24V, 12V, 5V, 3.3V) to various onboard components, ensuring reliable operation. Designed for high efficiency and low noise, it is essential for the sensitive instrumentation within the system.

Input Voltage Range: 20V - 30V DC (from High-Capacity Battery Pack)

Output Voltages: 24V, 12V, 5V, 3.3V DC

Maximum Current (24V Output): 5A

Maximum Current (12V Output): 8A

Maximum Current (5V Output): 10A

Maximum Current (3.3V Output): 5A

Efficiency: >90% (typical at full load)

Output Ripple & Noise: <20mVpp (24V, 12V), <10mVpp (5V, 3.3V)

Quiescent Current: <50mA (no load)

Thermal Shutdown: 160°C

Pins:

24V Input

24V Output

12V Output

5V Output

3.3V Output

Ground

Physical / Print
Dimensions: 150x100x25mm

Connections:

<img width="903" height="837" alt="image" src="https://github.com/user-attachments/assets/bae04fe5-29c1-4a03-a3d0-000a88a93882" />

Stepper Motor Driver (Trinamic TMC5160 Multi-Axis) – 

<img width="500" height="281" alt="image" src="https://github.com/user-attachments/assets/0865731a-1f15-4418-944b-1916b589efeb" />

Controls stepper motors for positioning the SQUID gantry.

Estimate: 1 × $200.00 = $200.00

Sourcing Options:

https://www.digikey.com/en/products/detail/trinamic-motion-control-gmbh/TMC5160-EVAL/8440398
https://www.newark.com/trinamic/tmc5160-eval/eval-board-stepper-motor-bipolar/dp/50AC9674
https://export.farnell.com/trinamic-analog-devices/tmc5160-eval/eval-board-stepper-motor-controller/dp/2846896

Description:
Controls multiple stepper motors for the robotic arm or gantry system to scan the SQUID sensors.

Technical Specifications:

The Trinamic TMC5160-EVAL is an evaluation platform for the TMC5160 high-power stepper motor controller and driver IC. It provides precise control for 2-phase bipolar stepper motors, offering advanced features like high microstepping and various current control modes. This board is essential for developing and testing motion control solutions for multi-axis robotic or gantry systems.

Operating Voltage (Motor Supply): 8 V to 60 V DC

Max Motor Current (RMS per phase): Up to 3 A (4.2 A peak)

Supported Motor Type: 2-Phase Bipolar Stepper Motors

Microstepping Capability: Up to 256 microsteps per full step

Control Interfaces: SPI, Step/Dir, UART

Number of Axes: 1 (per TMC5160 chip, eval board may integrate multiple)

Pins:

24V Power Input

Motor Outputs (x4)

SPI Control Input

Step/Dir Inputs

Physical / Print
Dimensions: 100x60x15mm

Connections:

<img width="1091" height="591" alt="image" src="https://github.com/user-attachments/assets/3c00745f-3afa-436d-a631-decdff8ff944" />

Gantry Frame (Aluminum Extrusions and Lead Screws) –

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/7d0b1c3a-ca8f-429e-acd2-612a88cdd100" />

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/0b68b8b7-f9dc-4814-a24c-a83bda276e0f" />

A rigid non-magnetic aluminum structure (base plate, vertical & horizontal 80×40 V-slot extrusions) supporting an X-Y gantry. The X-axis uses a precision lead screw (T8 2mm pitch) and linear rails (HIWIN) for smooth motion. A NEMA stepper motor with flexible coupler drives the lead screw.

Main Base Platform – 

<img width="500" height="422" alt="image" src="https://github.com/user-attachments/assets/6597fcb7-07ad-425d-a12a-3ddd5f6900f0" />

Heavy-duty 5083 aluminum plate.

Vibration Isolation Feet (M8 mounts) –

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/d8d85b18-3d7f-4634-bd35-53769bc7c52a" />

Rubber/spring isolators under the base.

Magnetic Shielding
Mu-metal Shielding Panels –

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/697f5b87-6305-490e-a1a4-2adc4bc246b8" />

High-permeability alloy sheets that surround the cryostat to block external magnetic fields.

3D-Printed Panel Holders and Clips –

<img width="1014" height="598" alt="image" src="https://github.com/user-attachments/assets/ecf8a366-fe92-4e13-825c-d240fd1385af" />

<img width="1546" height="599" alt="image" src="https://github.com/user-attachments/assets/2dfd25b5-48cb-4ded-b0f0-98cfdb39749f" />

Custom plastic mounts that secure the mu-metal panels and organize cables.

Miscellaneous Hardware – 

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/cb9b05c7-12c4-4141-9559-6cc04dec7600" />

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/aeb7d040-49bb-4382-9e6d-00f302514cf1" />


T-nuts, bolts, standoffs, and cable management clips (many parts are 3D-printed) used for assembly and cable routing.
The Bill of Materials (BOM) CSV provides details (names, quantities, descriptions). Typical parts from the BOM include high-end lab instruments (e.g. Zurich Lock-In, Keithley SMU), specialized sensors and electronics, and a mix of off-the-shelf mechanical parts and custom 3D-printed mounts. All components are chosen to be non-magnetic (aluminum, carbon fiber) near the sensor to avoid interference.
SQUID Cryostat Outer Housing-

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/9f33bf55-18fc-414a-bf25-995cca22db28" />

Custom Fabricated Carbon Fiber Housing
Estimate: 1 × $1500.00 = $1500.00

Sourcing Options:

https://fairclothcomposites.com/products/custom-parts
https://dragonplate.com/custom-carbon-fiber-fabrication
https://www.mcmaster.com/search?q=carbon+fiber+sheet

Description:
Lightweight, non-magnetic carbon fiber housing for the SQUID sensor array and integrated cryocooler.

Technical Specifications:
Physical / Print
Dimensions: 250x250x200mm
Material: Carbon Fiber

Connections:

<img width="1096" height="629" alt="image" src="https://github.com/user-attachments/assets/2df2c3bd-4f76-4c6d-8aac-699bdbcdec7b" />

Mechanical Assembly
Assemble the mechanical frame and mounts in the following order:

Base and Support Frame: Place the Main Base Platform on a stable surface. Attach the Vibration Isolation Feet to the base using M8 bolts. Insert M5 T-nuts into the grooves of the base and bolt the two Gantry Vertical Extrusions upright onto the base with M5 bolts and corner brackets. Ensure the vertical beams are square and evenly spaced.

Horizontal Cross-Members: Attach Gantry Horizontal Extrusions between the vertical supports using M5 bolts and corner brackets (one at the top, one near the middle height). This forms the upper frame.

Linear Rails and Lead Screw: On the horizontal extrusion, mount the X-Axis Linear Rails (HIWIN HGH20CA) with M3 screws. Install the X-Axis Lead Screw into bearings at the ends of the horizontal beam. The lead screw should run the length of the X-axis span. Slide the Linear Carriage onto the rail. The carriage will carry the SQUID cryostat.

Lead Screw Nut and Coupling: Attach the Lead Screw Nut to the linear carriage (use the custom 3D-printed mount). Connect the lead screw to the nut. At one end of the lead screw, attach the Lead Screw Coupler to connect to the stepper motor.

Stepper Motor Mounting: Mount the NEMA stepper motor on the base platform so that its shaft aligns with the lead screw. Use the Flexible Shaft Coupler (5mm to 8mm) to join the motor shaft to the lead screw. Tighten set screws securely.

Electronics Enclosure: Fix the Main Electronics Enclosure (Hammond aluminum box) to the base platform using screws. Inside the enclosure, mount the electronics boards: insert M3 standoffs on the 3D-printed board mounts to hold the Pre-Amplifier, RF Filter, Lock-In Amp board, ADC, FPGA, Jetson module, Wireless card, PDU, and Motor Driver PCBs. Each board goes on its designated mount (see schematics in hardware/). Use brass standoffs and screws to secure each board.

Cryostat and Sensor: Attach the SQUID Cryostat Outer Housing to the X-axis carriage using the custom 3D-printed “squid_cryostat_mount_3d” bracket. Inside the cryostat, install the SQUID Sensor Array onto the SQUID Sensor Mount (3D-printed). Ensure the sensor is centered and oriented correctly. Install the Cryocooler (Gifford-McMahon cold head) into its 3D-printed mounting bracket and fix it to the cryostat housing. This provides cooling to the SQUID. The cold head flange should sit firmly against the sensor stage.

Magnetic Shielding: Surround the cryostat with the Mu-Metal Shielding Panels. Slide each panel into place around the cryostat, then clamp them using the Mu-Metal Panel Holders (3D-printed clips). This forms a tight magnetic shield around the sensor.

Cable Management: Install the Cable Management Clips along the vertical extrusions, base, and around the enclosure interior. Route each cable (power, analog, digital) through the clips to keep them neat and to minimize movement. For example, bundle the SQUID signal cable from the cryostat to the preamp, and the cryocooler power cable down the frame, securing them every 50–100 mm.

Final Checks: Verify that all mechanical fasteners (M3/M5/M8 bolts, nuts, set screws) are tight. The linear carriage should move smoothly when the lead screw turns, with no binding. All 3D-printed mounts should hold components firmly without flex.

After assembly, you should have a structure as illustrated in the design: a gantry with an X-axis carriage carrying the cryostat, and an electronics enclosure on the base (see Project Images). The SQUID is suspended in the center of the mu-metal shield, with the cryocooler attached. The Jetson computer and all boards are inside the enclosure.

Electrical Connections
Wire up the power and signal connections as follows. Refer to the Electrical Connections diagram for pinouts.

Power Distribution: Connect the 24 V battery pack to the Main Power Distribution Unit (PDU) input. The PDU has multiple outputs:

24 V to the Step Motor Driver (Trinamic) – powers the stepper motors.
19 V to the Embedded AI System (Jetson) – via its power input jack. This powers the Jetson module.
5 V & 12 V to the FPGA/DSP Board – supply the Zynq SoC (via its barrel jack and auxiliary input).
5 V to the High-Resolution ADC Module.
+5 V and –5 V rails to the Pre-Amplifier Array (the ADA4807 preamps require dual supply).
AC Input to the Cryogenic Power Supply (Keithley) – the Keithley requires AC to drive the SQUID bias source.
240 VAC to the Cryocooler – the cryocooler has a separate mains power input. (In practice, one channel of the PDU output is wired through an AC inverter or transfer to deliver the cryocooler’s 240 VAC requirement.)
3.3 V to the Wireless Module (from a regulator or the Jetson’s internal M.2 power).
SQUID Bias: The Keithley 2400 SourceMeter (SQUID Cryogenic Power Supply) receives AC input from the PDU, and its DC output (variable voltage/current) goes to the SQUID Sensor Array. Connect the Keithley’s output terminals to the SQUID bias leads. This supplies the stable, low-noise current needed to operate the SQUID.

Analog Signal Chain: Use shielded coaxial cables for all low-level analog lines.

Connect the output of the SQUID array (sensor leads) to the inputs of the Pre-Amplifier Array. Each SQUID channel has an analog output port (these may be twisted-pair or coax outputs on the cryostat) – run these to the matching analog input connectors on the preamp board.
From the Pre-Amplifier Array, route the amplified signals to the RF Filter Array. The filter board inputs match the preamp outputs (e.g. SMA or BNC connectors).
From the RF Filter Array outputs, connect to the Lock-In Amplifier input channels. The lock-in provides demodulated outputs on its analog outputs.
Finally, connect the lock-in’s analog outputs to the inputs of the High-Resolution ADC Module. The AD7768 evaluation board has analog input pins; wire each lock-in output to the corresponding ADC input channel.
Digital and Control Signals:

Connect the ADC Module to the FPGA/DSP Board. For example, use SPI or LVDS links as per your design (the AD7768 can interface over SPI). Ensure the FPGA board is configured to receive the ADC’s digital data.
Connect the FPGA/DSP Board to the Jetson AI System over the PCIe bus. The Zynq’s onboard PCIe root port is wired to the Jetson’s PCIe slot. This link is used for high-speed data transfer from the FPGA to the Jetson.
Connect the Wireless Module (M.2 Wi-Fi 6E card) to the Jetson’s M.2 slot or PCIe slot. Provide it with 3.3 V power (usually via the Jetson board) and antenna connectors on the enclosure.
Connect the Step Motor Driver to the Jetson’s GPIO/SPI interface. The Trinamic driver board expects SPI lines (MOSI/MISO/SCLK and CS) and some GPIOs for enable/dir from the Jetson. Wire these to the Jetson’s expansion header or USB-SPI adapter.
Route any ground (GND) and common reference lines so that all subsystems share a proper ground reference. Typically, chassis and earth grounds are tied at the PDU.
Sensors and Feedback: If there are encoders or limit switches on the gantry (not listed in BOM but possible), connect them to the motor driver or Jetson GPIO as needed.

After wiring, double-check:

Polarity of power lines (correct +/– rails to boards).
Shielding and grounding (connect cable shields to ground at one end).
Secure all connectors in place to avoid vibration loosening.
Software and Operation
The system software runs on the NVIDIA Jetson AGX Xavier NX (Ubuntu Linux). Typical workflow:

Boot and Initialization: Power on the battery and switch on the PDU. The Jetson will boot. Ensure the FPGA board powers up and loads its bitstream (this may be via QSPI/SD on the Zynq board). The lock-in amplifier and other instruments (Keithley) may need to be manually powered on and configured via their front panels or digital interface.

Cryocooler Start-Up: Turn on the cryocooler mains. Wait for it to reach operating temperature (~4 K for low-Tc SQUID) – this can take 30+ minutes. During this time, the SQUID array is at ambient temperature and inactive.

SQUID Bias and Calibration: Once cold, use the Keithley to apply a small bias current to the SQUID. Check the SQUID I–V curve and tune it to a sensitive operating point (for example, using the feedback coil if available). Record the zero-field output.

Analog Front-End Tuning: On the preamplifier and lock-in, set gains and reference frequencies. For example, if the SQUID signal is modulated at a specific frequency, set the lock-in’s reference to that. Adjust the preamp gain such that the output is within the ADC range.

Data Acquisition: Run the acquisition software on the Jetson. For example, if there is a Python script:

bash
Copy
cd software/
python3 run_acquisition.py --duration 60 --channels 4
This script might configure the FPGA, start collecting samples from the ADC, and log them. Data can be streamed over Wi-Fi to a laptop or saved to disk on the Jetson.

Motor Control: To scan across the chest, send motion commands from the Jetson to the motor driver. For example:

bash
Copy
python3 move_motor.py --axis x --steps 2000
Ensure the motor driver is enabled and set to the correct microstep settings. Always ramp speed to avoid vibrations.

Real-Time Processing: The FPGA handles decimation and demodulation. The Jetson may run signal processing (filtering, averaging) and AI inference (e.g. detecting arrhythmia patterns). The exact software depends on your algorithms.

Shutdown Procedure: To power down safely, stop data acquisition, park motors, turn off lock-in outputs, and turn off the cryocooler last (since warming up the SQUID slowly is safer than abrupt warming).

Example Code (illustrative, not from actual repo):

python
Copy
# Example: Acquire 10 seconds of data from 4 channels
import mcg_system
mcg = mcg_system.MCGController()
mcg.move_motor(axis='x', position=100)     # position the gantry
data = mcg.acquire(duration=10.0)          # return NumPy array of samples
mcg.save_to_file('recording1.h5', data)    # save measurements
Replace the above with your actual APIs as implemented.

File Structure:

A suggested repository layout is:

graphql: 


/ (project root)

├── README.md                # (this file)

├── LICENSE                  # License 

/hardware

│   ├── CAD/                 # 3D models and drawings of mechanical parts

│   └── schematics/          # circuit schematics (PCB/board files)

/electronics

│   ├── pcb_files/           # PCB design files for PCBs (preamp, filter, etc.)

│   └── BOM.csv              # Bill of Materials (provided)

/firmware

│   ├── fpga/                # HDL source for FPGA logic (Zynq processing)

│   └── dsp/                 # DSP code for any signal processing IP

/software

│   ├── jetson/              # Code for NVIDIA Jetson (Python/C++ apps)

│   └── drivers/             # Low-level drivers (if any) for boards

├── docs

│   ├── wiring_diagram.png   # Block diagrams of power/signal flow

│   └── user_manual.pdf      # Extended documentation

└── examples

    ├── acquire_example.py   # Example usage scripts
    
    └── config.yaml          # Sample config files
    
Each folder can have its own README describing its contents. For instance, electronics/README.md could detail the signal-chain schematics. Be sure to update the BOM.csv file if parts change, and include datasheets or links for each critical component in this documentation repository.


IGNORE THIS ONE AS ALWAYS , I DON'T KNOW WHAT I AM DOING 
