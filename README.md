 Disaster Search Robot (CoppeliaSim Simulation)
This project is a modified version of the **BubbleRob** tutorial in CoppeliaSim.  
The robot has been redesigned to act as a *disaster-response search robot* that navigates an enclosed environment, detects obstacles, and identifies “victims” using sensors.

The script is written in **Lua** and runs inside CoppeliaSim’s embedded script environment.

---

## 📌 Project Overview
The robot simulates a post-earthquake search scenario:

- The robot uses **two sensors**:
  1. **Obstacle proximity sensor** (used for navigation)
  2. **Victim-detection sensor** (detects a target object called `Person_To_Detect`)

- When the robot detects an obstacle:
  - It stops
  - Reverses briefly
  - Rotates
  - Continues forward

- When the robot detects a victim:
  - It prints a detection message to the console
  - It increments a "victims found" counter
  - The sensor changes color from light blue → yellow  
    (visual indicator)

- The robot is placed inside an enclosed “building” environment to prevent it from falling off the map and to simulate a real collapsed structure.

---

## 🧠 Features
### ✔ Autonomous Navigation  
Based on proximity sensor input:
- Moves forward normally  
- Backs up + rotates when obstacle detected  
- Uses speed slider UI for dynamic control

### ✔ Victim Detection  
The wide-range sensor identifies `Person_To_Detect` objects:
- Prints detection info  
- Tracks the number of victims found  
- Changes sensor color for feedback  

### ✔ Real-Time Visualization  
The simulation includes:
- **Trace lines** showing robot movement path  
- **Distance graph stream**  
- **Drawing objects** showing collision distance segments  

### ✔ Interactive UI  
A simple UI slider adjusts motor speed dynamically during the simulation.
