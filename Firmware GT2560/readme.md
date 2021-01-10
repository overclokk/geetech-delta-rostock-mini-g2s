
Avoid stepper motor deactivation
https://reprap.org/forum/read.php?352,632188
`#define DEFAULT_STEPPER_DEACTIVE_TIME 0`

Settings for dvr8825 stepper driver 1/32
https://blog.prusaprinters.org/calculator_3416/
`#define DEFAULT_AXIS_STEPS_PER_UNIT   {160, 160, 160, 230}`



// Torre A
G28 G1 X-[90*sin(60)] Y-[90*sin(30)] Z0
// Torre B
G28 G1 X[90*sin(60)] Y-[90*sin(30)] Z0
// Torre C
G28 G1 X0 Y-[BPR] Z0

sin(60) // 0,80901699437494742410229341718282
sin(30) // 0,45399049973954679156040836635787

// Torre A
G0 X-72.80 Y-40.80 Z1 // G0 X72.80 Y40.80 Z1

// Torre B
G0 X72.80 Y-40.80 Z1 // G0 X-72.80 Y40.80 Z1

// Torre C
G0 X0 Y90 Z1  // G0 X0 Y-90 Z1

C to B
G0 X72.80 Y40.80 Z1

A to C
G0 X-72.80 Y40.80 Z1

A to B
G0 X0 Y-90 Z1
