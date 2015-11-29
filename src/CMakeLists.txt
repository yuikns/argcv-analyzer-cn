ADD_EXECUTABLE(anzcn-simple anzcn-simple.cc)

ADD_DEPENDENCIES(anzcn-simple argcv)

TARGET_LINK_LIBRARIES(anzcn-simple argcv_static)
TARGET_LINK_LIBRARIES(anzcn-simple argcv_ir_index_static)
TARGET_LINK_LIBRARIES(anzcn-simple argcv_string_static)
TARGET_LINK_LIBRARIES(anzcn-simple argcv_sys_static)
TARGET_LINK_LIBRARIES(anzcn-simple argcv_wrapper_leveldb_static)
TARGET_LINK_LIBRARIES(anzcn-simple argcv_wrapper_ini_static)
TARGET_LINK_LIBRARIES(anzcn-simple argcv_storage_static)

TARGET_LINK_LIBRARIES(anzcn-simple pthread)

TARGET_LINK_LIBRARIES(anzcn-simple ${CRFPP_LIBRARY_STATIC})
TARGET_LINK_LIBRARIES(anzcn-simple ${LEVELDB_LIBRARY_STATIC})
TARGET_LINK_LIBRARIES(anzcn-simple ${MONGO_CXX_LIBRARY_STATIC})

SET_TARGET_PROPERTIES(anzcn-simple PROPERTIES OUTPUT_NAME "anzcn-simple")


########################################################################################



