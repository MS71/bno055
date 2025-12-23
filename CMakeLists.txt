idf_component_register(
    SRCS 
        "src/bno055.c"
        "src/bno055_priv.c"
    INCLUDE_DIRS
        "include"        # public headers only
    PRIV_INCLUDE_DIRS
        "src"            # private headers, if any
    REQUIRES
        log              # visible to dependents

    PRIV_REQUIRES
        driver
)

target_compile_definitions(${COMPONENT_LIB} PUBLIC BNO055_VERSION_STR=\"1.0.0\")
