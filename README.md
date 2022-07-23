# Ros-system-install
if we want install Oprating System Ros we need download VirtualBox because install virtual operating system                                                            
and you can install Ubuntu 16.04LTS in the virtualbox .

1- link download VirtualBox : https://www.virtualbox.org/wiki/Downloads 
                                                                                                                                                                       
<img width="960" alt="image" src="https://user-images.githubusercontent.com/85851678/180609487-8b0af81d-ed6f-43e4-ad60-f4f6066bdd43.png">
                                                                                                                                                                       
2- link install Ubuntu 16.04LTS :  https://releases.ubuntu.com/16.04/         
                                                                                                                                                                       
<img width="949" alt="image" src="https://user-images.githubusercontent.com/85851678/180609458-673afdf5-8fe6-4503-a4b3-d18267d5427d.png">

3- open the VirtualBox , create new system                                                                                                                             
                                                                                                                                                                       
<img width="551" alt="image" src="https://user-images.githubusercontent.com/85851678/180609677-b69d8d5c-af31-44f4-bf5c-520f5fa6ef69.png">
                                                                                                                                                                       
4- give name then click Next
                                                                                                                                                                       
<img width="308" alt="image" src="https://user-images.githubusercontent.com/85851678/180609795-6d501a81-daeb-4c2e-9816-9d23267473a6.png">
                                                                                                                                                                       
5-Give a good memory space
                                                                                                                                                                     
<img width="310" alt="image" src="https://user-images.githubusercontent.com/85851678/180609903-052dc6f7-fcee-48a8-82a2-6a0c2d8b1441.png">
Click Next on all other pages to finish                                                                                                                             
                                                                                                                                                                     
then system ready click start                                                                                                                                           
<img width="553" alt="image" src="https://user-images.githubusercontent.com/85851678/180610099-bf2d6b1f-ad22-43e5-aa33-344a5311c824.png">
                                                                                                                                                                     
6- Select the downloaded file for Ubuntu                                                                                                                             
                                                                                                                                                                     
<img width="385" alt="image" src="https://user-images.githubusercontent.com/85851678/180610309-58a5ebfc-0766-4245-829c-c779ed070768.png">

7- install Ubuntu                                                                                                                                                   
                                                                                                                                                                     
<img width="479" alt="image" src="https://user-images.githubusercontent.com/85851678/180610453-6b2cbe9d-6bae-49c5-97ae-8973d4981db8.png">
8-Continue with the normal download process  

9-it is important save username and password                                                                                                                         
                                                                                                                                                                     
<img width="669" alt="image" src="https://user-images.githubusercontent.com/85851678/180610664-fc2d829e-c86c-49db-b002-aa3d20c3dc1c.png">
                                                                                                                                                                     
10- Now it's upload Ubuntu                                                                                                                                           
11- Now open Ubuntu                                                                                                                                                 
12- open website https://s-m.com.sa/ros.txt  This site has all the commands to download Ros                                                                         
13- open the terminal and write the commands

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'                          ////  Prepares the device to install a Ros

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update                                        ////  doing a system update

sudo apt-get install ros-kinetic-desktop-full             ////  install Ros Kinetic

apt-cache search ros-kinetic

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init    

rosdep update

sudo apt-get install ros-noetic-catkin

sudo apt-get install ros-kinetic-rosserial-arduino            ////  install Arduino IDE                                                                             
sudo apt-get install ros-kinetic-rosserial
                                                                                                                                                                     
cd <sketchbook>/libraries                                    ////   Install the ros_lib library on the Arduino program                                               
rm -rf ros_lib                                                                                                                                                       
rosrun rosserial_arduino make_libraries.py    


mkdir -p ~/catkin_ws/src         ////  We work here on Workspace and I give the name catkin_ws you can give any name you want

cd ~/catkin_ws/

catkin_make                     ////  I install the package for arm that I need in the project

cd ~/catkin_ws/src       

git clone https://github.com/smart-methods/arduino_robot_arm.git 

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-kinetic-moveit

sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line
(source /home/hissah/catkin_ws/devel/setup.bash)
then 
ctrl + o     ////   for out 

source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch              ////   He's going to work with me program Rviz
                                                                                                                                                                     
<img width="960" alt="arm" src="https://user-images.githubusercontent.com/85851678/180617267-149e86c2-a302-4f0c-8af0-7f7e17a800a3.png">
                                                                                                                                                                     
### In the end, the Ros software was downloaded and packagand the arm package we needed in the mission ran.


