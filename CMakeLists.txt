#=============================================================================#
# Author: Tauheed Elahee                                                      #
# Date:   2020-01-15                                                          #
#                                                                             #
# Description: Project to figure out arduino senosrs                          #
#                                                                             #
#=============================================================================#
set(CMAKE_TOOLCHAIN_FILE cmake/ArduinoToolchain.cmake) # Arduino Toolchain


cmake_minimum_required(VERSION 3.0)
#====================================================================#
#  Setup Project                                                     #
#====================================================================#
project(ArduinoExample C CXX)

print_board_list()
print_programmer_list()

add_subdirectory(src) # add the source directory
