# 1131 Robotics-EX
Training materials for the courses **[ME4609301] Introduction to Robotics Tutorial**
 and **[SI5302701] Autonomous Mobile Vehicles and Robots Introduction**
.
- ME4609301 Mechanical Engineering Department, Taiwan-Paraquay Polytechnic University
- SI5302701 Graduate Institute of Intelligent Manufacturing Tech., National Taiwan University of Science and Technology
####
🥇This training course utilizes two types of robots, EPSON C3-600 (C4-600) and ABB IRB 1090. The EPSON robots are the primary ones used to develop manipulating skills and the final project for students. The ABB robot was dedicated to the machine vision exercises in the second half of the semester. 
####
🥈Students start the basic exercises like picking-n-place and stacking with the robot (EPSON), then integrate I/O and accessories to achieve higher-level logical control and manipulating skills. The capability of using a robot is defined in five levels. Each level represents the complexity of the operation the robotic system can handle.
#### 
🥉Optional 
- Option 1: ABB Machine Vision (**For ME4609301 only**)
  1. Feeder to Tray (in Field of Vision): Use the camera to identify the coordinates of cavities on the tray and conduct pick-and-place from feeder to tray. ( three tokens and three blocks)
  2. Random tokens (in Field of Vision) to Tray: Use the camera to identify the three tokens and three blocks randomly spread on the platform, pick them up, and place them back on the tray.  
- Option 2: Autonomous Mobile Robot, Jetbot **(For SI5302701 only)**
  - Build a Jetbot:  https://jetbot.org/master/index.html   
## Contents: 
- Refer to 1121 Robotic course https://github.com/iiotntust/1121robot/tree/main
- ABB station wiring https://github.com/imintust/1131_robotics-EX/blob/main/ABB_wire/schematic.jpg (suspending)
# ABB Robot Tutorial
## Basic operation and machine vision
Exercises:
- Day 1 Basic ABB robot Operation 
  - Briefing (Day 1 handout)
  - Install ABB Robot studio
  - Demo pick-and-place
    - Simulator: https://youtu.be/RzuO8K04AFg; IRB 1090 - https://youtu.be/-G4bnbylSYE  
  - Teaching Pendant practice (each team 30 mins)
    - **Work object coordinate** setting practice 
 - Day 2 Machine Vision
    - Task 1: Tray localization:
    - Task 2: Token Localization  
 - Day 3
    - optimized the image processing to promote the accuracy
    - Complete the pick-n-place tasks with machine vision    

## Software installation - ABB robotstudio
### Software RobotStudio Suite:
- https://new.abb.com/products/robotics/robotstudio
## Hardware Robot - ABB IRB 1090
### :small_blue_diamond: Schematic and I/O Wiring diagram 
- Schematic:
- I/O Wiring diagram:  
### :small_blue_diamond: ABB Robot Manuals
1. Robot Manual:
    https://new.abb.com/products/robotics/robots/articulated-robots/irb-1090
## Controller OmniCore E10 Controller:
- https://new.abb.com/products/robotics/controllers/omnicore/omnicore-e10




## :feet: Resources (CAD files, manuals):
CAD software, files, and manuals.
### :small_blue_diamond: CAD software
1. Mechanical Engineering Department - CAD software 
https://www.me.ntust.edu.tw/p/405-1005-35690,c2568.php?Lang=zh-tw
2. Free auto cad, register with student ID. 
https://www.autodesk.com/products/fusion-360/education
3. Education account apply
https://www.autodesk.com/education/support

### :small_blue_diamond: CAD files (tool, fixture, tray…)
1. Tooling End Effector: https://a360.co/44fONAx 
2. Token: https://a360.co/3pmQSv7
3. Block: https://a360.co/3NmZcTH
4. Fixture, Tray: https://a360.co/3JyIhw6
5. Alignment/Infeed fixture: https://a360.co/3NNyUKD
6. Reference Point Setup Tool: https://a360.co/3PyeMhJ

### :small_blue_diamond: CAD files from vendors, Chelic. (Solenoid, Gripper, vacuum nozzle)
1. Chelic components download: https://chelic.partcommunity.com/

### :small_blue_diamond: EPSON manuals
## 3.Manual and Reference
1. EPSON manual:
chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://files.support.epson.com/far/docs/epson_rc_pl_70_users_guide-rc700a_rc90_t(v73r4).pdf  
2. Delta HMI manual: chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://filecenter.deltaww.com/Products/download/06/060302/Manual/DELTA_IA-HMI_DOPSoft_UM_EN_20211230.pdf
### :small_blue_diamond: Demo video
1. Calibration exercise: local/tool coordinates calibration: https://youtu.be/TOrHTE-4aC4
2. Task 1: pick and place (feeder-->fixture-->tray): https://youtu.be/XQcib0vzzIk
3. Task 2: Stacking https://youtu.be/oQTrqzth1_I
4. I/O box assembly: https://youtu.be/_gBvWF14sqk
