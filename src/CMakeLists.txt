include_directories(${CMAKE_SOURCE_DIR}/include)

#Recursive libraries must be declared.
#set(Ucglib_RECURSE True)

set(ARDUINO_DEFAULT_BOARD leonardo) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyACM0) # Default Port, when not specified

generate_arduino_firmware(Blink
    SKETCH Blink
    PROGRAMMER avrispmkii
    PORT /dev/ttyACM0
    SERIAL picocom @SERIAL_PORT@ -b 115200 -l)