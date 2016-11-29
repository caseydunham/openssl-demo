cmake_minimum_required(VERSION 3.7.0)

project(ssldemo)

find_package(OpenSSL REQUIRED)
message("OpenSSL include dir: ${OPENSSL_INCLUDE_DIR}")
message("OpenSSL libraries: ${OPENSSL_LIBRARIES}")

set (SOURCE_FILES
  src/ssldemo.cpp
)

include_directories(${OPENSSL_INCLUDE_DIR})

add_executable(ssldemo ${SOURCE_FILES})

target_link_libraries(ssldemo ${OPENSSL_LIBRARIES})
