cmake_minimum_required(VERSION 3.00)
project(CORE)

set(CMAKE_CXX_STANDARD 17)

ADD_SUBDIRECTORY(Bullets)
ADD_SUBDIRECTORY(Enemies)
ADD_SUBDIRECTORY(Hero)
ADD_SUBDIRECTORY(Other)
ADD_SUBDIRECTORY(Player)

ADD_DEPENDENCIES(Enemies Bullets Other)
ADD_DEPENDENCIES(Hero Bullets Other)
ADD_DEPENDENCIES(Bullets Other)
ADD_DEPENDENCIES(Player Hero)