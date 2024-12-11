# Elevator Control System Simulation
> *.pdsprj* can be open with Proteus8

## Overview
This project involves the design and implementation of a control system simulating the operation of a 4-floor elevator. The system includes inputs and outputs to mimic real elevator functionality, including buttons, display lights, motor control, and door operations. The program is developed in assembly language.

## Features
1. **Inputs and Outputs**:
   - Floor call buttons (up and down) with corresponding indicator lights.
   - Internal elevator buttons for target floors (4 floors) with corresponding indicator lights.
   - Display of elevator status (up, down, stop) and current floor.
   - Motor control for elevator movement.
   - Door open/close functionality.

2. **Key Functions**:
   - Respond to button presses and update LED and display indicators.
   - Determine the next operation based on a scheduling algorithm.
   - Simulate elevator motion using a stepper motor for precise floor movements.
   - Automatically return to the first floor after prolonged inactivity.
   - Extended functionality includes internal open/close door buttons.

## Hardware Design
### Components
- **Keyboard Matrix**: Represents call and floor buttons.
- **LEDs**: Indicate button states.
- **7-Segment Display**: Shows elevator status, current floor, and door state.
- **Stepper Motor**: Simulates elevator motion.
- **74LS595 Chip**: Expands control ports for managing LED indicators.

### Port Allocation
- **P0**: Keyboard matrix interface.
- **P1**: 
  - Low nibble: 7-segment display control.
  - High nibble: Stepper motor control.
- **P2**: 7-segment display data.
- **P3**: 
  - Low nibble: LED control via 74LS595.
  - High nibble: Direct LED control.

## Software Design
### Development Approach
- **Modular Design**: Functions for each component (buttons, LEDs, display, motor) were implemented and tested individually before integrating into the main program.
- **Control Logic**: Implements elevator scheduling, state management, and safety features (e.g., preventing door operation while moving).

### Testing
- Verified individual button functionality.
- Integrated LEDs and tested button-to-LED mapping.
- Ensured correct 7-segment display outputs.
- Validated stepper motor operation for floor movements.
- Debugged and fine-tuned the main control logic, addressing edge cases and conflicts.

## Challenges and Solutions
1. **Stepper Motor Control**: Issues with erratic rotation were resolved by redesigning the timer and fixing wiring errors.
2. **LED Display**: Initial attempts with the 74LS138 decoder failed due to simulation limitations; switching to 74LS595 provided stable and continuous LED output.
3. **Code Organization**: Managing 1000+ lines of assembly code was challenging. Improved variable tracking and debugging practices were applied.

## Project Highlights
- A fully functional 4-floor elevator simulation with robust and user-friendly features.
- Enhanced understanding of stepper motor control, LED management, and modular programming in assembly.
- Improved debugging skills and problem-solving techniques in hardware-software integration.

## Future Improvements
- Better code structuring and documentation for ease of maintenance and readability.
- Enhanced scalability to support additional floors with minimal modifications.
- Streamlined debugging and testing workflows to reduce development time.

## Conclusion
This project was completed independently, from hardware circuit design to code implementation. It demonstrated the challenges and satisfaction of creating a fully functional system from scratch. The final product met design expectations and provided valuable insights for future projects.
