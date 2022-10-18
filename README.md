# tmotor-python-can-lib

Use the following command to set the CAN bitrate in baud

`sudo ip link set can0 type can bitrate 1000000`

and use the command

`sudo ip link set up can0`

to enable the CAN interface.

To install the library navigate to the directory containing `setup.cfg` and run 

`pip install .`

To use the library use

`from motor_driver.canmotorlib import CanMotorController`

and initial a motor object with 

`motor = CanMotorController(can_socket='can0', motor_id=0x01, motor_type='AK80_64')`