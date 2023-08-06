cmake_minimum_required(VERSION 3.23)
project(GameRecommender)

set(CMAKE_CXX_STANDARD 14)

find_package(CURL CONFIG REQUIRED)

add_executable(GameRecommenderFromSteamProfile main.cpp bptree.cpp gameData.cpp node.cpp)

target_link_libraries(GameRecommenderFromSteamProfile PRIVATE CURL::libcurl)
