rock_library(canopen_master
    SOURCES NMT.cpp SDO.cpp StateMachine.cpp Emergency.cpp PDO.cpp
        PDOMapping.cpp Exceptions.cpp Slave.cpp
    HEADERS Frame.hpp NMT.hpp SDO.hpp StateMachine.hpp Exceptions.hpp
        Emergency.hpp PDO.hpp PDOMapping.hpp PDOCommunicationParameters.hpp
        Slave.hpp Objects.hpp
    DEPS_PKGCONFIG canbus base-types)

rock_executable(canopen_ctl Main.cpp
    DEPS canopen_master)
