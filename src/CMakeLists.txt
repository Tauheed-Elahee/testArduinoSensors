set(ARDUINO_DEFAULT_BOARD uno)
set(ARDUINO_DEFAULT_PORT /dev/ttyACM0)

link_directories(../arduino_libraries/Adafruit_Sensor)
link_directories(${ARDUINO_SDK_PATH}/libraries/Wire)
set(Wire_RECURSE True)
link_directories(${ARDUINO_SDK_PATH}/libraries/SPI)
set(SPI_RECURSE True)
link_directories(../arduino_libraries/Adafruit_BMP280)

generate_arduino_firmware(arduino_sensors
    SRCS main.cpp
    PORT /dev/ttyACM0
    BOARD uno
)
