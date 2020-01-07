# camera_setup(kinect 360)

sudo apt-get install libfreenect-dev

sudo apt-get install ros-kinetic-freenect-launch

roslaunch freenect_launch freenect.launch depth_registration:=true

# camera_setup(kinect one)

install libfreenect2

https://github.com/OpenKinect/libfreenect2

to install without cuda

cmake .. -DCMAKE_INSTALL_PREFIX=$HOME/freenect2 -DENABLE_CUDA=OFF

if cannot build protonect
../lib/libfreenect2.so.0.2.0: undefined reference to `XRRSetCrtcGamma'
../lib/libfreenect2.so.0.2.0: undefined reference to `XRRGetOutputInfo'

do 

locate libglfw

take /usr/lib/x86_64-linux-gnu/libglfw.so.3.1

edit CMakeCache.txt in build

//Path to a library.

GLFW3_LIBRARY:FILEPATH=/usr/lib/x86_64-linux-gnu/libglfw.so.3.1

if no permission

sudo cp ../platform/linux/udev/90-kinect2.rules /etc/udev/rules.d/

install iai_kinect2

https://github.com/code-iai/iai_kinect2
