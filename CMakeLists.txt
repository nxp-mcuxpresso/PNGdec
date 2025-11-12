
if (CONFIG_MCUX_COMPONENT_middleware.pngdec)
    mcux_add_source(
        SOURCES src/adler32.c
                src/crc32.c
                src/crc32.h
                src/infback.c
                src/inffast.c
                src/inffast.h
                src/inffixed.h
                src/inflate.c
                src/inflate.h
                src/inftrees.c
                src/inftrees.h
                src/PNGdec.c
                src/PNGdec.h
                src/zconf.h
                src/zlib.h
                src/zutil.c
                src/zutil.h
    )
    mcux_add_include(
        INCLUDES src
    )
    mcux_add_iar_configuration(
        CC "--diag_suppress=Pe111"
    )

    mcux_add_mdk_configuration(
        CC "-Wno-deprecated-non-prototype"
    )
endif()
