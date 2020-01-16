set(ARDUINO_DEFAULT_BOARD uno)
set(ARDUINO_DEFAULT_PORT /dev/ttyACM0)

link_directories(${ARDUINO_SDK_PATH}/libraries)
link_directories(../arduino_libraries)

generate_arduino_firmware(arduino_sensors
    LIBRARY Adafruit_BMP280
    SRCS main.cpp
    PORT /dev/ttyACM0
    BOARD uno
)
