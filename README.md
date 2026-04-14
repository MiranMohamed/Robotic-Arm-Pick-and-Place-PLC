# Industrial Robotic Arm Pick-and-Place System (ST)

## Project Description
This project implements an industrial robotic arm pick-and-place system using Structured Text (ST) in CODESYS.

The system detects objects on a conveyor, picks them using a robotic arm, and places them at a designated location. The operation is controlled using a state machine, timers, counters, and safety mechanisms.

---

## System Workflow

1. The conveyor moves objects forward.
2. A sensor detects an object at the pick-up position.
3. The robotic arm moves from home to the pick-up position.
4. The gripper closes to pick the object.
5. The arm moves to the drop-off position.
6. The object is released.
7. The arm returns to the home position.
8. A counter increments for each processed object.

---

## Control Strategy

- The system is implemented using a state machine (`currentState`) to control sequence execution.
- Timers (TON) are used for:
  - Arm movement delays
  - Gripping and releasing operations
- A counter (CTU) is used to track processed items.
- Sensors are used for object detection and positioning.
- Actuators control the robotic arm and gripper movement.

---

## Mathematical Modeling

The system incorporates basic mathematical models within the control logic:

- Conveyor speed calculation:
  V = D / T

- Robotic arm motion using linear interpolation:
  Pt = Pi + (Pf - Pi) × (t / T)

- Gripper force calculation:
  Fg = m × g × SF

---

## Safety Features

- Emergency stop immediately halts:
  - Conveyor motor
  - Arm movement
  - Gripper operation
- All timers and counters are reset
- System returns to initial safe state

---

## Demo Video

https://drive.google.com/file/d/1XVcq5G-Cf6nQatvReGPA7xr3EwphK9zy/view?usp=drive_link
