project(find)

find_package(Qt4 REQUIRED)
include(${QT_USE_FILE})
include_directories(${CMAKE_CURRENT_BINARY_DIR} )
QT4_WRAP_CPP(find_mocs finddialog.h)
########### next target ###############

set(find_SRCS 
  finddialog.cpp
  main.cpp
  ${find_mocs}
  )
add_executable(find ${find_SRCS})

target_link_libraries(find ${QT_LIBRARIES} )

# install(TARGETS find  ${INSTALL_TARGETS_DEFAULT_ARGS} )

########### install files ###############

# install( PROGRAMS kblocks.desktop  DESTINATION  ${XDG_APPS_INSTALL_DIR} )
# install( FILES kblocks.kcfg  DESTINATION  ${KCFG_INSTALL_DIR} )
# install( FILES kblocksui.rc  DESTINATION  ${DATA_INSTALL_DIR}/kblocks )
# install( FILES kblocks.knsrc  DESTINATION  ${CONFIG_INSTALL_DIR} )

# kde4_install_icons( ${ICON_INSTALL_DIR}   )



