add_library (drs4data SHARED src/DRS4_fifo.cxx
                             src/DRS4_writer.cxx
                             src/DRS4_reader.cxx
                             src/DRS4_data.cxx
                             )

target_include_directories(drs4data PUBLIC include ${DRS4_INCLUDE_DIRS} ${ROOT_INCLUDE_DIRS} )
target_link_libraries ( drs4data PRIVATE ${ROOT_LIBRARIES})

install( TARGETS drs4data LIBRARY DESTINATION lib )

