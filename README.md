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
