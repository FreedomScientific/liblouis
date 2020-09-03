configure_file(config.h.in config.h)

add_LIBRARY(liblouis SHARED
commonTranslationFunctions.c
compileTranslationTable.c
logging.c
lou_backTranslateString.c
lou_translateString.c
maketable.c
metadata.c
pattern.c
utils.c)
if (WIN32)
target_sources(liblouis PRIVATE ${PROJECT_BINARY_DIR}/liblouis.rc)
endif()
target_include_directories(liblouis PUBLIC "${PROJECT_BINARY_DIR}")
