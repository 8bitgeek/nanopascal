project(nanopascal)

set(PASCALSRC
    ${PROJECT_SOURCE_DIR}/src/ast.cpp
    ${PROJECT_SOURCE_DIR}/src/functiondefs.cpp
    ${PROJECT_SOURCE_DIR}/src/parser.cpp
    ${PROJECT_SOURCE_DIR}/src/pcodegenerator.cpp
    ${PROJECT_SOURCE_DIR}/src/reader.cpp
    ${PROJECT_SOURCE_DIR}/src/symboltable.cpp
    ${PROJECT_SOURCE_DIR}/src/tokenizer.cpp
    ${PROJECT_SOURCE_DIR}/src/vmtypes.cpp
)

set(VMSRC 
    ${PROJECT_SOURCE_DIR}/virtualmachine/main.c
    ${PROJECT_SOURCE_DIR}/virtualmachine/vm.c
)

add_executable(vm ${VMSRC})
add_executable(nanopascal ${PASCALSRC})
