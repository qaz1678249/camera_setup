# camera_setup(kinect 360)

sudo apt-get install libfreenect-dev

sudo apt-get install ros-kinetic-freenect-launch

roslaunch freenect_launch freenect.launch depth_registration:=true
