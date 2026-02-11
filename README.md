# Project2: URDF and Gimbal Lock
This project was intended to learn about the Unified Robot Description Format from ROS. Additionally, we were tasked with demonstrating the "gimbal lock" phenemenon that occurs when using Euler angles to describe 3-dimensional roataion. This project uses a simple URDF model of EVE from the Pixar movie WALL-E. Additionally, the URDF of R2D2 from Star Wars that was included in the original URDF tutorial in included for testing purposes.

## Usage
1. Create a ROS2 workspace with a `src` folder.
2. Clone this repository into the `src` folder.
3. Navigate back to the main folder of your workspace.
4. Build the repository with the following command.
   ```
   colcon build --packages-select Project2_rabeckes
   ```
5. Run the Rviz configuration with the launch file.
   ```
   ros2 launch Project2_rabeckes eve.launch.xml
   ```

## Gimbal Lock
Gimbal lock is a phenemenon that happens when using Euler angles (yaw, pitch, roll) to describe 3-dimensional rotation. When two of these axis are aligned, they become locked and a degree of freedom is lost. In effect, the changing of the angle of two of the axis will result in the same rotation. This phenemenon is demonstrated below with the EVE URDF design. When the roll and pitch of the arm are aligned to 90 degrees (positive or negative), the roll and yaw angles become locked and cause the same rotation. These angles will continue to be locked until the yaw is moved away from 90 degrees "unlocking" the roll in the process.

![axis alignment](https://github.com/Robust-Autonomous-Systems-Laboratory/Project2_rabeckes/blob/main/images/alignment.png)

![gimbal lock](https://github.com/Robust-Autonomous-Systems-Laboratory/Project2_rabeckes/blob/main/images/gimbal_lock.gif)
