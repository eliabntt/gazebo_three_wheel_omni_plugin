# A plugin to control 3-wheels omnidirectional robot in gazebo

This plugin was developed due to the lack of control availability for such kind of robots. 
It will take velocity commands and translate that to realistic movement of the platform, with odometry (with or without noise) and producing the whole TF tree and correct transformations in the environment.

Although developed in a rush, it should have all the topics/information exposed as ros parameters/args.

The work was developed to a standard 3-wheeled omnidirectional robot.

To use with your robot please _disable_ friction between the wheels and the environment.

Then attach to the robot, in order, an _{x,y,yaw}_joints_ with the yaw joint that should be the parent of your "visual" block.

It takes a `cmd_vel` command in input and translate that to wheels' joint velocities.

The robot will move controlled by PID controllers, one for each joint. The wheels will rotate _realistically_ but WILL **NOT** produce friction.

Odometry will be published both as grountruth and as a noisy odometry. The TF tree will be updated accordingly.

For any issue do not esitate and open an issue.

The code was developed within the [iRotate](https://github.com/eliabntt/irotate_active_slam) project. If you find it useful please consider checking our other works and cite us.

## License

All Code in this repository - unless otherwise stated in local license or code headers is

Copyright 2021 Max Planck Institute for Intelligent Systems, Tübingen.

Licensed under the terms of the GNU General Public Licence (GPL) v3 or higher. See: https://www.gnu.org/licenses/gpl-3.0.en.html
