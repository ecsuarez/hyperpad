set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Find Qt
find_package(Qt6 COMPONENTS Core Widgets REQUIRED)

# Executable
add_executable(hyperpad)

# Link
target_link_libraries(hyperpad PRIVATE
    Qt6::Core
    Qt6::Widgets
)


# Sources
target_sources(hyperpad
    # Headers
    PUBLIC
    mainwindow.hpp
    io.hpp
    texteditor.hpp
    statusbar.hpp
    # Sources
    PRIVATE
    main.cpp
    mainwindow.cpp
    io.cpp
    texteditor.cpp
    statusbar.cpp
    # UI files
    mainwindow.ui
    # Resources
    # Add resources
    ${CMAKE_SOURCE_DIR}/data/resources.qrc
)
