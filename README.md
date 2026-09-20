# **OHM FORCE NIGHTLAMP**

Project Technical Documentation & Circuit Specification

# **AIM**

To design and construct an energy-efficient, automatic nightlamp circuit utilizing a photodiode sensor module, NPN transistor switch, and a high-efficiency Red LED that automatically illuminates during low ambient light conditions and switches off in daylight.

# **PROJECT DESCRIPTION**

The Ohm Force Nightlamp is an automated light-sensing circuit engineered to act as an intelligent ambient lighting solution. Traditional nightlamps require manual switching, leading to unnecessary power consumption when ambient light is adequate.

&nbsp;

This circuit addresses that inefficiency by incorporating a light detection mechanism. The photodiode module continuously monitors the surrounding light intensity. Under daylight or ambient room light, the photodiode maintains low resistance or sends a high control signal, keeping the transistor in a cutoff state (OFF). As ambient light diminishes, the photodiode's operational state changes, driving voltage to the base of the transistor through a biasing resistor network (100 kohm). Once the base-emitter voltage reaches the threshold , the transistor acts as a closed switch, allowing current to flow through the current-limiting resistor (1 kohm) to illuminate the Red LED.

# **MATERIALS REQUIRED**

| Component | Specification / Value | Description & Function |
| :---- | :---- | :---- |
| **Photodiode Module** | Light-sensitive sensor module | Detects ambient light levels and generates a corresponding electrical signal to drive the switching logic. |
| **Transistor** | NPN (e.g., BC547) | Operates as an electronic switch, amplifying the small control current from the sensor to switch the LED load. |
| **Resistor 1** | 100 kohm | Acts as a base biasing resistor to set the switching threshold and sensitivity of the transistor circuit. |
| **Resistor 2** | 1 kohm | Serves as a protective current-limiting resistor for the Red LED, preventing excess current burn-out. |
| **Output Indicator** | Red LED | Serves as the primary light source, providing visual indication and illumination when the system detects darkness. |
| **Power Supply** | 5 DC Battery or Adaptor | Provides necessary operational DC voltage to bias the transistor and power the LED indicator. |
| **Prototyping Hardware** | Breadboard & Jumper Wires | Facilitates solderless circuit assembly and connections during testing and prototyping. |

# **WORK FLOW**

1. **Light Detection Stage**: The photodiode module continuously samples light levels in the surrounding environment.  
2. **Signal Conversion & Biasing**:  
   * **In Bright Light**: The photodiode allows minimal voltage to reach the transistor base. The base voltage remains below , keeping the transistor in the **Cutoff Region** (OFF state).  
   * **In Darkness**: The photodiode's resistance rises or its module output toggles, directing current through the  biasing resistor into the transistor base.  
3. **Switching Activation**: When the base voltage exceeds the transistor enters the **Saturation Region** (ON state), completing the path from the collector to the emitter.  
4. **Load Illumination**: Current flows from the power source, passes through the protective ONE Kohm resistor, and energizes the Red LED, producing a steady light output.  
5. **Automatic Reset**: When ambient light returns, the sensor restores the low base voltage, switching the transistor OFF and extinguishing the Red LED.

# **APPLICATIONS**

* **Home Automation**: Nighttime pathway and hallway safety lighting.  
* **Energy Conservation**: Automatic street lights and decorative porch lights that eliminate daytime power wastage.  
* **Security Systems**: Low-cost darkness-activated indicator or deterrence lights.  
* **Educational Demonstrations**: Basic electronics training for transistor switching and optoelectronic sensing.

# **SHEMATIC CIRCUIT**

![acircuit.jpeg](acircuit.jpeg)

# **CIRCUIT**

![Circuit.jpeg](Circuit.jpeg)

# **RESULTS**

\`![result](Resulta.jpeg)![result](Result.jpeg)

&nbsp;

# **DEMO**

https://drive.google.com/file/d/1xYViuhGsAt1XboobROiZTpPMqTuAu5po/view?usp=sharing

# **NOTES**

* **Polarity Verification**: Ensure correct pin configurations for the transistor (Collector, Base, Emitter) and correct anode/cathode orientation for the Red LED before applying power.  
* **Sensitivity Calibration**: The 100 kohm resistor determines the sensitivity threshold. A potentiometer can replace this fixed resistor if manual calibration to specific ambient light levels is desired.  
* **Current Protection**: Never bypass the 1 kohm series resistor connected to the Red LED, as direct battery voltage will damage the light-emitting diode.  
* **Power Supply Stability**: Ensure a stable DC power source within to maintain consistent switching performance and prevent false triggering under flickering ambient conditions.

&nbsp;
