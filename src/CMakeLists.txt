ADD_EXECUTABLE(anzcn anzcn.cc)

ADD_DEPENDENCIES(anzcn argcv)


# http://www.gnu.org/software/libc/manual/html_node/Feature-Test-Macros.html#index-_005fPOSIX_005fSOURCE 
#ADD_DEFINITIONS( " -D_POSIX_SOURCE ") 
#INCLUDE(ExternalProject) # IF NEED EXTEND PROJECT
#INCLUDE(ExternalLeveldb)
#MESSAGE(STATUS "$$$$$$$$$$ INCLUDE LEVELDB DIR " ${LEVELDB_INCLUDE_DIR})
#INCLUDE_DIRECTORIES(${LEVELDB_INCLUDE_DIR})

TARGET_LINK_LIBRARIES(anzcn argcv_static)
TARGET_LINK_LIBRARIES(anzcn argcv_ir_index_static)
TARGET_LINK_LIBRARIES(anzcn argcv_string_static)
TARGET_LINK_LIBRARIES(anzcn argcv_sys_static)
TARGET_LINK_LIBRARIES(anzcn argcv_wrapper_leveldb_static)
TARGET_LINK_LIBRARIES(anzcn argcv_wrapper_ini_static)
TARGET_LINK_LIBRARIES(anzcn argcv_storage_static)
#TARGET_LINK_LIBRARIES(anzcn argcv_wrapper_curl_static)

TARGET_LINK_LIBRARIES(anzcn pthread)

TARGET_LINK_LIBRARIES(anzcn ${CRFPP_LIBRARY_STATIC})
TARGET_LINK_LIBRARIES(anzcn ${LEVELDB_LIBRARY_STATIC})
TARGET_LINK_LIBRARIES(anzcn ${MONGO_CXX_LIBRARY_STATIC})



#  executable properties
SET_TARGET_PROPERTIES(anzcn PROPERTIES OUTPUT_NAME "anzcn")




