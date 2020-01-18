set(ARDUINO_DEFAULT_BOARD uno)
set(ARDUINO_DEFAULT_PORT /dev/ttyACM0)

link_directories(../arduino_libraries/ArduinoCore-avr/libraries/Wire)
set(Wire_RECURSE True)
link_directories(../arduino_libraries/ArduinoCore-avr/libraries/libraries/SPI)
set(SPI_RECURSE True)
link_directories(../arduino_libraries/Adafruit_Sensor)
link_directories(../arduino_libraries/Adafruit_BMP280)
link_directories(../arduino_libraries/DHT)

generate_arduino_firmware(arduino_sensors
    SKETCH ../arduino_libraries/DHT/examples/DHTtester
    #SRCS main.cpp
    PORT /dev/ttyACM0
    BOARD uno
)
