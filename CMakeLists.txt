cmake_minimum_required(VERSION 3.0)

include("HunterGate.cmake")

HunterGate(
	URL "https://github.com/ruslo/hunter/archive/v0.14.23.tar.gz"
	SHA1 "999f07d004649f5f549953f74f21e46b48d53931"
	)

project(repro)

hunter_add_package(Boost COMPONENTS system filesystem)

set(Boost_USE_STATIC_LIBS ON)

find_package(Boost CONFIG REQUIRED system filesystem)

add_executable(foo foo.cpp)

target_link_libraries(NoobEdit PUBLIC Boost::boost Boost::system Boost::filesystem)
