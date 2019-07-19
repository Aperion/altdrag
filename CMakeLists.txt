cmake_minimum_required(VERSION 3.13)

project(hooks)
add_library(hooks
        hooks.c
        include/hooks.rc)

project(altdrag)
add_executable(altdrag
        altdrag.c
        include/altdrag.rc)

target_link_libraries(altdrag
        hooks
        shlwapi
        wininet
        comctl32)

project(import_languages)
add_executable(import_languages
        tools/import_languages.c)
target_link_libraries(import_languages
        shlwapi)

project(HookWindows_x64)
add_executable(HookWindows_x64
        hookwindows_x64.c
        include/HookWindows_x64.rc)


