# Source files that need to be compiled
set(SRCS
    EPM.cpp
    Solution.cpp
    Utils/Physics.cpp
    Models/Original/Model.cpp
    Models/Original/StateObserver.cpp
    Models/Original/Integrate.cpp
    Models/Original/RHS.cpp
    Models/External.cpp
    )

# This command ensures the static library gets build
add_library(EPM STATIC ${SRCS})

# This command defines the dependencies of libEPM.a
target_link_libraries(EPM AIM Core Util)
