### robot.Camera

Class that represents a camera
 - **Methods**
  - see( ): returns a list of [markers](#robotmarker) currently visible to the camera.


 - **Properties**
  - serial: the camera's serial number.

---

### robot.CartCoord
Class that represents a set of cartesian coordinates
 - **Properties**
  - x: x-axis cartesian coordinate in meters.
  - y: y-axis cartesian coordinate in meters.
  - z: z-axis cartesian coordinate in meters.

---

### robot.Marker
Class that represents a marker
 - **Methods**
    - is_token_marker( ): returns true if the marker is a token, false if otherwise.
    - is_wall_marker( ): returns true if the marker is a wall, false if otherwise.


 - **Properties**
  - cartesian: a [CartCoord](#robotcartcoord) object representing the cartesian coordinates of the marker relative to the robot.
  - distance_meters: the distance to the marker in meters.
  - id: the id number of the marker.
  - pixel_centre: pixel coordinates of the centre of the marker.
  - pixel_corners: pixel coordinates of the corners of the maker.
  - polar: a [PolarCoord](#robotpolarcoord) object representing the polar coordinates of the marker relative to the robot.
  - size: size of the marker in meters.

---

### robot.Motor
Class that represents a motor
 - **Properties**
   - voltage : the normalised voltage of the motor.

---   

### robot.MotorBoard
Class that represents a motor board
 - **Properties**
  - m0: The [motor](#robotmotor) connected to m0 on the motor board.
  - m1: The [motor](#robotmotor) connected to m1 on the motor board
  - serial: the board's serial number.

---

###  robot.PolarCoord
Class that represents a set of polar coordinates
 - **Properties**
  - distance_meters: distance to the point in meters.
  - rot\_x_deg: rotation on the x axis in degrees.
  - rot\_y_deg: rotation on the y axis in degrees.
  - rot\_z_deg: rotation on the z axis in degrees.
  - rot\_x_rad: rotation on the x axis in radians.
  - rot\_y_rad: rotation on the y axis in radians.
  - rot\_z_rad: rotation on the z axis in radians.

---

###  robot.PowerBoard
Class that represents a power board
 - **Methods**
  - power_on( ): turns the power on to the connected boards.
  - power_off( ): turns the power off to connected boards.


 - **Properties**
  - serial: the board's serial number.

---

###  robot.Robot
Class that represents the robot as a whole
 - **Properties**
  - cameras: a dictionairy of connected [Cameras](#robotcamera), using their serial numbers as keys.
  - motor_boards: a dictionairy of connected [Motor Boards](#robotmotorboard), using their serial numbers as keys.
  - power_boards: a dictionairy of connected [Power Boards](#robotpowerboard), using their serial numbers as keys.
  - servo_boards: a dictionairy of connected [Servo Board](#robotservoboard), using their serial numbers as keys.

---

###  robot.Servo
Class that represents a servo
 - **Properties**
  - position: the position of the servo.

---

###  robot.ServoBoard
Class representing a servo board
 - **Properties**
  - ports: returns a list of up to sixteen [servos](#robotservo), indexed by port number.
  - serial: Serial number for the board.

---
### Data Values
Constant data values found inside the robot library.
 - BRAKE: used by [motors](#robotmotor) to tell it to break
 - COAST: used by [motors](#robotmotor) to tell it to coast
 - GOLD_TOKEN: a list of the id numbers of all gold token markers
 - POISON_TOKEN: a list of the id numbers of all poison token markers
 - SILVER_TOKEN: a list of the id numbers of all silver token markers
 - TOKEN: a list of the id numbers of all token markers
 - WALL: a list of the id numbers of all wall markers.