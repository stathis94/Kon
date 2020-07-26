file(GLOB applications applications/*.cpp)
file(GLOB sources src/*.cpp)
file(GLOB includes include/*.h)

set(target main)

include_directories(include/)

add_library(myLibrary SHARED ${sources} ${includes})

add_executable(${target} ${applications})

target_link_libraries(${target} ${myLibrary})
