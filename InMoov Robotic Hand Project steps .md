### InMoov Robotic Hand Project - README

Welcome to the InMoov Robotic Hand project! This README will guide you through the process of building, assembling, and controlling a 3D-printed robotic hand using the InMoov design. The project involves 3D printing the components, assembling them, and setting up the electronics and software to bring the hand to life.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Required Components](#required-components)
3. [3D Printing the Parts](#3d-printing-the-parts)
4. [Circuit Diagram](#circuit-diagram)
5. [Assembly Instructions](#assembly-instructions)
6. [Testing and Calibration](#testing-and-calibration)
7. [Additional Resources](#additional-resources)
8. [Contributing](#contributing)
9. [License](#license)

## Project Overview

The InMoov Robotic Hand is an open-source project designed for 3D printing and DIY enthusiasts. The hand is designed to be a low-cost yet highly functional prosthetic or robotic hand. It uses servomotors, controlled via microcontrollers, to mimic human hand movements.

## Required Components

### Hardware
- **3D Printed Parts**: Refer to the [InMoov website](https://inmoov.fr/hand-and-forarm/) for STL files.
- **Servomotors**: 5x MG996R or equivalent.
- **Microcontroller**: Arduino Uno or similar.
- **Power Supply**: Appropriate power source for servos and microcontroller.
- **Wiring**: Assorted wires for connections.
- **Fasteners**: Screws and nuts compatible with the printed parts.

### Tools
- **3D Printer**: Capable of printing ABS or PLA.
- **Screwdriver set**
- **Soldering kit** (optional but recommended for solid connections)
- **Pliers and cutters**

## 3D Printing the Parts

1. **Download the STL Files**: Get the latest STL files from the [InMoov website](https://inmoov.fr/hand-and-forarm/).
2. **Prepare the 3D Printer**:
   - Material: ABS or PLA
   - Layer height: 0.1-0.2 mm for finer detail
   - Infill: 20-30% for strength and flexibility
3. **Print the Parts**: Ensure proper bed adhesion and print settings are calibrated for your material.

## Circuit Diagram

Below is a simplified circuit diagram for connecting the servomotors to the Arduino:

```
                 +----+          +---------+
                 |    |          |         |
            +5V  |    |----------| VCC     |
                 |    |          |         |
    Microcontroller|  |          | Servo 1 |
       (Arduino) |    |          |         |
            GND  |    |----------| GND     |
                 |    |          |         |
            PWM1 |    |----------| Signal  |
                 |    |          +---------+
                 |    |              .
                 |    |              .
            PWM2 |    |          +---------+
                 |    |          |         |
                 +----+          | Servo 5 |
                                 |         |
                                 +---------+
```

- **PWM1 - PWM5**: Connect to digital pins on the Arduino (e.g., 9, 10, 11, 12, 13).
- **VCC**: Common 5V power supply for all servos.
- **GND**: Common ground.

## Assembly Instructions

1. **Finger Assembly**:
   - Attach the servomotors to the base of each finger as indicated in the InMoov guide.
   - Use appropriate screws to secure the joints.
   
2. **Palm and Wrist Assembly**:
   - Connect the fingers to the palm piece.
   - Attach the wrist servomotor and connect the assembly to the forearm.

3. **Electrical Connections**:
   - Connect the servomotors to the Arduino as per the circuit diagram.
   - Ensure all servos are properly powered and grounded.

4. **Testing Joints**:
   - Manually check the flexibility and movement of each joint.

## Testing and Calibration

1. **Initial Testing**: Power on the system and check if all servos are responding correctly.
2. **Calibration**: Adjust the servo positions in the code to fine-tune finger movements.

## Additional Resources

- **InMoov Forum**: For community support and discussions.
- **YouTube Tutorials**: Search for "InMoov hand assembly" for visual guidance.

## Contributing

Feel free to fork this repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

*This README provides a basic overview and steps to build and assemble the InMoov robotic hand. For more detailed instructions and troubleshooting, refer to the official [InMoov website](https://inmoov.fr/hand-and-forarm/).*
