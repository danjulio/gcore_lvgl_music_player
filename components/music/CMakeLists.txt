file(GLOB SOURCES *.c assets/*.c)

idf_component_register(SRCS ${SOURCES}
                       INCLUDE_DIRS . assets ../lvgl
                       REQUIRES lvgl)
                       
target_compile_definitions(${COMPONENT_LIB} INTERFACE LV_CONF_INCLUDE_SIMPLE=1)