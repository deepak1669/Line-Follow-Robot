Features
  Uses 2 IR sensors (left & right)
  Smooth line tracking with tunable speed control
  Adjustable motor trimming for straight movement
  Simple and optimized logic for beginners
  Compatible with L298N / motor driver modules


  
How It Works
The robot continuously reads values from the IR sensors:

Left Sensor	    Right Sensor  	  Action
White          	White	Move        Forward
White          	Black	Turn        Right
Black          	White	Turn        Left
Black          	Black             Stop



Pin Configuration

IR Sensors
  Right IR Sensor → Pin 11
  Left IR Sensor → Pin 12
  
Motor Driver (L298N or similar)
Motor	Arduino Pin
  ENA (Right Speed)	6
  IN1	7
  IN2	8
  ENB (Left Speed)	5
  IN3	9
  IN4	10


  
Adjustable Parameters
  #define MOTOR_SPEED   130
  #define TURN_SPEED    150
  #define RIGHT_TRIM    -10
  MOTOR_SPEED → Base forward speed
  TURN_SPEED → Turning strength
  RIGHT_TRIM → Fix drifting (left/right imbalance)


  
Getting Started
  Connect all components as per the pin configuration
  Upload the code to Arduino
  Place the robot on a black line over a white surface
  Power the robot and watch it follow the line


  
Components Required
  Arduino UNO (or compatible)
  2 × IR Sensors
  L298N Motor Driver
  2 × DC Motors + Wheels
  Chassis
  Battery Pack


  
Future Improvements
  Add PID control for smoother movement
  Integrate Bluetooth control
  Add obstacle detection
  Include buzzer or LED indicators


  
Logic Function Used

  The rotateMotor() function controls:

  Motor direction (forward/backward)
  Speed using PWM signals


  
License
This project is open-source and free to use.
