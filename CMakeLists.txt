cmake_minimum_required(VERSION 3.5)
project(sandbox)

add_subdirectory(src/vendor/rabbitmq-c)

set(SOURCE_FILES src/main.cpp)
add_executable(AMQPSTest ${SOURCE_FILES})
target_link_libraries(AMQPSTest rabbitmq-c ${CMAKE_THREAD_LIBS_INIT})
