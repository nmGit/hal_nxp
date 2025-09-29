if (CONFIG_MCUX_COMPONENT_driver.clock)
    mcux_component_version(2.5.3)

    mcux_add_source(
        SOURCES fsl_clock.h
                fsl_clock.c
    )

    mcux_add_include(
        INCLUDES .
    )

endif()

if (CONFIG_MCUX_COMPONENT_driver.iomuxc)
    mcux_component_version(2.0.4)

    mcux_add_source(
        SOURCES fsl_iomuxc.h
    )

    mcux_add_include(
        INCLUDES .
    )

endif()

add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/flexram)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/romapi)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/nic301)