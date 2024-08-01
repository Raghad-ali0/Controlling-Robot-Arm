# Controlling-Robot-Arm
Controlling Robot Arm
## First i well creat and build a catkin workspace
by using these commands:

 ``` $ mkdir -p ~/catkin_ws/src ```  ````  $ cd ~/catkin_ws/ ```` ````` $ catkin_make `````
 
![unnamed-13](https://github.com/user-attachments/assets/52025382-d331-4d48-ac6c-6d388ea4c0a7)

### here use this command to look in your current directory you should now have a 'build' and 'devel' folder :
```
ls
```
![unnamed-14](https://github.com/user-attachments/assets/1e97766a-5af1-4878-beae-d0f7fea13527)

#### source your new setup.*sh file:

```
source ~/catkin_ws/devel/setup.bash
```
Run command :
```
gedit ~/.bashrc
```
here you can see that at the end of the page that apeared the source line we applied earlier
```
source ~/catkin_ws/devel/setup.bash
```
![unnamed-11](https://github.com/user-attachments/assets/766fef4d-9c6f-44d2-b7f0-d38ba76bc235)

#### Install arduino robot arm Package:

first apply command``` cd src ```then apply the following command:
```
 sudo apt install git
```
![unnamed-10](https://github.com/user-attachments/assets/2e348b43-fc87-434b-b356-4d5629e3ba9a)

- Use this to link the library with your project:
```
git clone https://github.com/smart-methods/arduino_robot_arm
```
- Next step is going back to `` catkin_ws ``  ````by using cd````  command:
  - Then try using this:
    ```
    rosdep install --from-paths src --ignore-src -r -y
    ```
- Use command:
 ```
 sudo apt-get install ros-noetic-moveit
 ```
![unnamed-9](https://github.com/user-attachments/assets/5e9d8ebd-2dd5-4851-b7ba-ddc1f5ef0303)

 -Use this command:
 ```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
![unnamed-8](https://github.com/user-attachments/assets/6da2473d-b8d3-4c84-ae14-498d28c0f348)

- Use command:
 ```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
![unnamed-7](https://github.com/user-attachments/assets/376e11f1-53d6-4e78-8672-8953deba0bd4)

- Use command:
```
catkin_make
```
![unnamed-6](https://github.com/user-attachments/assets/e2419f6b-77df-4369-9a60-15e723798c35)

##### launch and Control Motors:
```
roslaunch robot_arm_pkg check_motors.launch
```
![unnamed-5](https://github.com/user-attachments/assets/1bc09c39-34c6-468b-8648-8f45aecd1beb)

![unnamed-4](https://github.com/user-attachments/assets/2e002c27-6aa9-4206-830d-b21b37fe6704)

###### MoveIt Motion Planning Framework:
```
roslaunch moveit_pkg demo.launch
```
![unnamed-3](https://github.com/user-attachments/assets/b6555a46-5b35-44b6-b150-b8c1c696d940)

####### Gazebo simulator:
```
roslaunch robot_arm_pkg check_motors_gazebo.launch

```
![unnamed-2](https://github.com/user-attachments/assets/cfd67566-7b3f-460e-9180-0d6e02b8d6a4)
![unnamed](https://github.com/user-attachments/assets/224aedb2-97eb-40d7-9718-ac884197a653)
