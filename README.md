# Eclipse to VS Code port of 2018 code for Iron Plaid 3103
In order to get this to build, deploy, and function (or at least get the RIO to see the robot class), the following steps appeared to be necessary:
1. After upgrade step, the folders were placed too deeply under another set of main/java folders - had to move the actual main/ folder back to be under src/
2. There seemed to be two versions of code - main/ and org/ - the one under main/ couldn't possibly have built, so we determined the source under org/ to be the correct source, and deleted main/
3. While the code would then build and deply, the RIO couldn't see the robot class.  Couldn't figure out why, so we just renamed the folders to a main/java/frc structure, fixed package declarations, and it seemed to do the trick.

This code has not yet been tested on a fully built robot.

# 2018PowerUpCode
Subsystems: 
	BoxCatcher
    - moveFoward()
    - moveBack()
    - turnWheel()
  Elevator
    - moveUp()
    - moveDown()
  Winch 
    - rotate()
  LimeLight
    - lightOn()
    - lightOff()
Automate: 
  - seek and get box and stop
  - 4 set positions for elevator
  - intake and retract 
Autonomous:
  - move forward 
  - deliver box to scale 
  - deliver box to switch
Sensors needed: 
  - limit switch 
  - absolute encoder 
  - gyroscope 
OI: 
  - different driving modes 
