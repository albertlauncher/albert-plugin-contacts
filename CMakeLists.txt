if(APPLE)

cmake_minimum_required(VERSION 3.16)
project(contacts VERSION 6.1)

find_package(Albert REQUIRED)

find_library(CONTACTS_FRAMEWORK Contacts)

albert_plugin(
    LINK PRIVATE ${CONTACTS_FRAMEWORK}
    QT Widgets Concurrent
)

target_compile_options(${PROJECT_NAME} PRIVATE "-fobjc-arc")

endif()
