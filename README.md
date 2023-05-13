# AM8-Config-Chimera

This is the config I created for my Chimera setup with the BIGTreeTech SKR 1.3 Motherboard

Things to remember:
Configuration.h
* #define STRING_CONFIG_H_AUTHOR "(mgollop, AM8 config 10 May 2023)
* #define SERIAL_PORT -1
* #define SERIAL_PORT_2 0
* #define MOTHERBOARD BOARD_BTT_SKR_V1_3
* #define CUSTOM_MACHINE_NAME "AM8 Printer"
* #define MACHINE_UUID "3b995e65-8bdf-49bc-bef1-6f1106123fca"
* #define EXTRUDERS 2
* #define HOTEND_OFFSET_X { 0.0, 18.00 }
* #define TEMP_SENSOR_1 1
* #define TEMP_SENSOR_BED 1
* #define PID_PARAMS_PER_HOTEND
* #define DEFAULT_Kp_LIST {  23.51,  28.23 }
* #define DEFAULT_Ki_LIST {   1.66,   2.14 }
* #define DEFAULT_Kd_LIST { 83.23, 93.07 }
* #define PIDTEMPBED
* #define DEFAULT_bedKp 177.01
* #define DEFAULT_bedKi 23.42
* #define DEFAULT_bedKd 891.82
* #define X_MIN_ENDSTOP_INVERTING true
* #define Y_MIN_ENDSTOP_INVERTING true
* #define X_DRIVER_TYPE  TMC2130
* #define Y_DRIVER_TYPE  TMC2130
* #define Z_DRIVER_TYPE  TMC2130
* #define E0_DRIVER_TYPE TMC2130
* #define E1_DRIVER_TYPE TMC2130
* #define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 400, 412.90 }
* #define USE_PROBE_FOR_Z_HOMING
* #define BLTOUCH
* #define NOZZLE_TO_PROBE_OFFSET { -22, 17, -2.33 }
* #define INVERT_X_DIR true
* #define INVERT_Y_DIR false
* #define INVERT_Z_DIR true
* #define X_BED_SIZE 220
* #define Y_BED_SIZE 220
* #define X_MIN_POS -14
* #define AUTO_BED_LEVELING_UBL
* #define RESTORE_LEVELING_AFTER_G28
* #define PREHEAT_BEFORE_LEVELING
* #define G26_MESH_VALIDATION
* #define Z_SAFE_HOMING
* #define EEPROM_SETTINGS
* #define SDSUPPORT
* #define REPRAP_DISCOUNT_FULL_GRAPHIC_SMART_CONTROLLER

Configuration_adv.h
* #define BABYSTEPPING
* #define MONITOR_DRIVER_STATUS
* #define HYBRID_THRESHOLD
* #define SENSORLESS_HOMING
* #define TMC_USE_SW_SPI
* X_STALL_SENSITIVITY  7
* Y_STALL_SENSITIVITY  7
* #define TMC_DEBUG

Tuning UBL - note ensure M875 is set to bed level not 0.2 or 0.3:
G29 P1 T  #Probe the points
G29 P3 R C .5 # figure out any spaces

