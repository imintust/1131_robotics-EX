# 1131 Robotics-EX
Training materials for the courses **[ME4609301] Introduction to Robotics Tutorial**
 and **[SI5302701] Autonomous Mobile Vehicles and Robots Introduction**
.
- ME4609301 Mechanical Engineering Department, Taiwan-Paraquay Polytechnic University
- SI5302701 Graduate Institute of Intelligent Manufacturing Tech., National Taiwan University of Science and Technology
####
🥇This training course utilizes two types of robots, EPSON C3-600 (C4-600) and ABB IRB 1090. The EPSON robots are the primary ones used to develop manipulating skills and the final project for students. The ABB robot dedicated to the machine vision exercises in the second half of the semester. 
####
🥈Students start the basic exercises like picking-n-place and stacking with the robot (EPSON), then integrate I/O and accessories to achieve higher-level logical control and manipulating skills. The capability of using a robot is defined in five levels. Each level represents the complexity of the operation the robotic system can handle.
#### 
🥉Optional 
- Option 1: ABB Machine Vision (**For ME4609301 only**)
  1. Feeder to Tray (in Field of Vision): Use the camera to identify the coordinates of cavities on the tray and conduct pick-and-place from feeder to tray. ( three tokens and three blocks)
  2. Random tokens (in Field of Vision) to Tray: Use the camera to identify the three tokens and three blocks randomly spread on the platform, pick them up, and place them back on the tray.  
- Option 2: Autonomous Mobile Robot, Jetbot **(For SI5302701 only)**
  - Build a Jetbot:  https://jetbot.org/master/index.html   
## Contents table
#### 1.Exercises (tasks):
  - Basic tasks, Challenging tasks, Final exam tasks (competition), Level of Capability:
#### 2.Resources:
  - Demo program (pick-n-place), 3D models (End-effector, Fixtures, Tray, token), I/O Wiring diagram, HMI, 3D printer
#### 3.Manuals and Reference:
  - EPSON robot, ABB robot (For ME4609301), Jetbot (For SI5302701 course)
#### 4.Demo Video 
## 1. Exercises (Tasks)
### :triangular_flag_on_post: Basic and Challenging tasks
The suggested basic tasks can help students familiarize the setting of the World, Local, and Tool coordinates with the robots and utilize essential functions and commands.
The challenging tasks provide ideas and drill exercises for students to improve their coding and planning skills. These tasks only depicted the targets (specification or functionality) without detailed instructions. Students should use their creativity to leverage the functions and commands they learned in the lectures and robot manuals.

### Basic tasks
- Task 1. Exploring the robot envelop and the work cell:
Install tools and components (feeder, fixture, tray) and explore their coordinates with tools (extra parts may be required to proceed with the calibration)
1. Define the World (local0), Local, tool(tool0), tool coordinates. (Based on the robots and works cell)
2. Measure the tool dimension and the center offset between tool0(J6, robot) and tools.(Tool1: gripper, Tool2: vacuum nozzle)
3. Decide the space between "objects"(tokens and blocks) at pick-up and approach gap when place

Exercise: Transfer tokens from the feeder to the fixture first, then move them to the tray. 
- Task 2. Building the simulation environment:

There are two ways to build the simulation environment:
1. Use the measured dimension of the robot envelope and the work cell in Basic: Task 1.
2. Start a new layout arrangement with the CAD files
Exercise: Insert CAD models in a robot envelope. 

### Challenging tasks

- #### Task 1. Tools
1. Gripper - high accuracy (can skip the alignment process in specific circumstances); can be used as a tool to align objects at fixtures (alignment)
2. Vacuum nozzle - with the pressure sensor, can be used to check objects and as a tool to align objects. 
3. Explore the status by vacuum pressure gauge (sensor): check feeder, fixture, and tray status. (quantity, occupied or vacancy)
- #### Task 2. Feeder
1. Two feeders (A, B)
2. Mixed tokens and blocks
3. Stack up not neatly (not aligned)
4. Unfull-fill the feeder (checking quantity)
- #### Task 3. Fixture
1. Two fixtures are primary and secondary (as buffer when there is no space at the tray).  
2. Rotate the block in (20 mm x 24 mm) or (24 mm x 20 mm); from the unaligned block pile in Challeng task 2-3.
3. Develop a way to detect the orientations of the block (20 mm x 24 mm); it might be a gripper or vacuum nozzle. 
- #### Task 4. Tray
1. One tray - keep status in robot memory (occupied or vacancy)
2. Two trays, one at the essential location and one at another with an angle(30 degrees). 
- #### Task 5. GUI
- ##### A. Functionality: 
1. GUI#1 - stack up tokens and blocks alternately at fixture (from feeder to fixture); one button to stack and the other to unstack.
2. GUI#2 - Move tokens and blocks into the tray from feeder to tray (fixture optional); one button forward and one return.
- ##### B. Tools: 
1. I/O box: Start (Green), Reset (Org), Stop (Red); Forward(Blue), Reverse(White)
2. HMI: create the button on the touchscreen
3. EPSON robot GUI: create the button on the touchscreen
  
- #### Task 6. Others (optional)
- ##### A. Response to unexpected issues: 
1. Lose power
2. Lose pneumatic (or low-pressure)
3. Los I/O signal (hardware malfunction)
4. Emergency Stop 
- ##### B. Function button or GUI - to complete operation cycle:
1. Auto mode / manual mode
2. Reset function 
3. Self-awareness (diagnosis)

### 📈  Final exam tasks (competition):
Each team should complete the following tasks in 30 minutes. 
1. Basic Task 1: Pick-n-Place
   Criterion 
   - Completed the movement of three tokens and three blocks from the Feeder to the Fixture and then to the Tray by order.   
   - Conduct the movement reversely, from Tray to Feeder directly. (Skip the fixture cell)
   Score
   - Total Time (the team with the shortest time wins)
2. Basic Task 2: Stack-up
   Criterion 
   - Stack up tokens and blocks alternatively. (five tokens and five blocks)  
   Score
   - Total Time (the team with the shortest time wins)
3. Integration task: (refer to the challenging tasks)
   - Create at least self-design fixtures
   - Integrate I/O box or HMI in process
   - Other Creativity 

### 📈  Level of Capability:

To measure the capability of implementation of a robotic project.

|     **Level**    |   **Capbility**  |**Example assignments** |
|:------------------:|:------------------------------:|:---------:|
| 01   | Can set coordinates (world, local, tools) and align tool to work cell.| Complete basic tasks, like the six pieces pick-n-place task (one feeder, one fixture, one tray)
| 02   |Can communicate with a robot to perform selection or make some judgment via I/O or network | manually conduct select feeder, sort token, and block via HMI. (in practice, the robot can communicate to the end effectors ( like a screwdriver, soldering gun, glue nozzle, welding torch, etc.; or machine vision to get the location or OCR information|
| 03   |Can plan process to handle expected changes| When one feeder is empty, it automatically changes to the other. |
| 04   |Can handle unexpected changes| When lost power, lost pneumatic, E-Stop, can restore system by interference.|
| 05   |Can perform continuous operation with auto restore capability response to anomaly detection and continue to operate | Automatically drop the token or block when an anomaly is detected and restored. |  

The goal is to make the robot run automatically without human intervention. The program should also be flexible enough to accommodate various processing changes.  
## 2.Resources:
### :joystick: Mechanical design and assembling: (group A and B collaboration)
In this sector, students learn how to design the mechanical parts for the gripper on the robot and the cylinder on the peripherals and print and assemble them on the robot system. 
- #### Gripper
1. Design "Finger"
2. 3D print  
3. Assembly
4. Github: drawing and files (for 3D printer).
- #### Cylinder
1. Design "Holder"
2. 3D print 
3. Assembly
4. Github: save drawings and files (for 3D printer).
- #### Instruction and reference
1. Instruction .ppt (follow TA)
2. 3D printer (Phrozen3)
   - Phrozen manual download (Sonic Mini 4K): https://phrozen3d.com/pages/manual
   - Test model file: https://phrozen3d.com/pages/phrozens-xp-finder-and-rp-tester-test-model-download-and-tutorials
   - Tutorial video: https://phrozen3d.com/pages/video-tutorial
   - Software download: https://phrozen3d.com/pages/software
   - Chitubox download: https://www.chitubox.com/en/download/chitubox-free
4. 3D printer (Roland)
   - Roland Technical Support: https://www.rolanddga.com/support/products/3d-printing-devices
   - Tutorial video: https://www.youtube.com/watch?v=uk_OII4pgcA
   - Taiwan Agent: http://www.twinsoft.com.tw/ARM-10/ARM10.htm  
### :eight_pointed_black_star: Electrical design and wiring: (group A and B collaboration)
In this sector, students learn how to illustrate the wiring diagrams for the I/O box and HMI and conduct the wiring and assembly to the I/O Bus of the EPSON robot.
- #### I/O box:
1. Illustrate wiring diagram (.pdf)
   - Cable to button(6): Red, Orange, Green (latch type); Blue, White (unlatch type); buzzer. 
   - I/O box to Robot I/O terminal
2. Wiring and Assembling
3. Github: save drawing and files (.pdf)
4. Reference:
   - Pushbutton Switch:[[reference link](https://www.amazon.com/Latching-Button-Switch-Waterproof-K16-371/dp/B0975WXFTB/ref=sr_1_17_sspa?crid=DO62EE9HW0YB&keywords=16mm%2BPush%2BButton%2BSwitch&qid=1694827804&sprefix=16mm%2Bpush%2Bbutton%2Bswitch%2Caps%2C303&sr=8-17-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9tdGY&th=1)]
   - Wiring (suggested: No.1, Button On/ LED on)https://github.com/imintust/1131_robotics-EX/blob/main/IO_box%20wire.png   
    
- #### HMI:
1. Illustrate wiring diagram
2. Wiring and Assembling
3. Github: save drawing and files (.pdf)
4. Reference
   - HMI (Weintek MT8072ip): software EasyBuilder Pro V6.02.02.248 (2019/06/28) https://www.weintek.com/globalw/Download/Download.aspx
   - Early version software: EasyBuilder8000 V4.66.02.016 (2016/12/21); for the sample code in class.
   - WEINTEK forum (EPSON): https://forum.weintekusa.com/t/epson/669
   - WEINTEK forum (EPSON)https://forum.weintekusa.com/t/epson-robot/665
   - WEINTEK HMI full course: [https://youtu.be/9YaUIj5ODLw?si=S0883oPlBQHvz60B](https://www.youtube.com/watch?v=PaFW0P7mkN8&list=PLAol9q3JCKsGbLue6MNgywZ9IXAbHMF4O)
- #### Wiring diagram
  - EPSON
  - ABB station wiring https://github.com/imintust/1131_robotics-EX/blob/main/ABB_wire/schematic.jpg
# Robot Machine visio Tutorial (ABB)
## Software installation - ABB robotstudio
### Software RobotStudio Suite:
- https://new.abb.com/products/robotics/robotstudio
## Hardware Robot - ABB IRB 1090
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
