# rg6_gripper_description
URDF file of onrobot rg6 gripper based on the repository of  [syuntoku14 /
fusion2urdf](https://github.com/syuntoku14/fusion2urdf.git) and the step file provided by [OnRobot](https://onrobot.com/en/downloads)

Visulazition is launched with display.launch
```
$ roslaunch rg6_gripper_description display.launch
```

Rviz:

![Alt text](/pictures/rviz.png?raw=true "Rviz")


Note:

If the defaulted angle between the adapter and the main body of the gripper has been changed custermlly, update rpy under the joint g_main in rg6_gripper.xacro:

```ruby
<joint name="g_main" type="fixed">
  <origin xyz="-0.031849 1e-06 0.04953" rpy="0 0 0"/>
  <parent link="base_link"/>
  <child link="g_main_1"/>
</joint>
```
