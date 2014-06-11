project(stasm)

cmake_minimum_required(VERSION 2.8)

find_package(OpenCV REQUIRED)

set(STASM_BASE_DIR "${CMAKE_CURRENT_SOURCE_DIR}" CACHE STRING "Stasm source directory")

add_library(stasm
${STASM_BASE_DIR}/stasm/asm.cpp
${STASM_BASE_DIR}/stasm/classicdesc.cpp
${STASM_BASE_DIR}/stasm/convshape.cpp
${STASM_BASE_DIR}/stasm/err.cpp
${STASM_BASE_DIR}/stasm/eyedet.cpp
${STASM_BASE_DIR}/stasm/eyedist.cpp
${STASM_BASE_DIR}/stasm/faceroi.cpp
${STASM_BASE_DIR}/stasm/hat.cpp
${STASM_BASE_DIR}/stasm/hatdesc.cpp
${STASM_BASE_DIR}/stasm/landmarks.cpp
${STASM_BASE_DIR}/stasm/misc.cpp
${STASM_BASE_DIR}/stasm/pinstart.cpp
${STASM_BASE_DIR}/stasm/print.cpp
${STASM_BASE_DIR}/stasm/shape17.cpp
${STASM_BASE_DIR}/stasm/shapehacks.cpp
${STASM_BASE_DIR}/stasm/shapemod.cpp
${STASM_BASE_DIR}/stasm/startshape.cpp
${STASM_BASE_DIR}/stasm/stasm.cpp
${STASM_BASE_DIR}/stasm/stasm_lib.cpp

${STASM_BASE_DIR}/stasm/MOD_1/facedet.cpp
${STASM_BASE_DIR}/stasm/MOD_1/initasm.cpp
)

target_link_libraries(stasm
  ${OpenCV_LIBRARIES}
)
