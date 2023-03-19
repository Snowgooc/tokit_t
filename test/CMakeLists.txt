CMAKE_MINIMUM_REQUIRED (VERSION 3.5)


# 设置编译选项
SET (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} --coverage -fno-access-control ")

SET (TEST_ROOT ${PROJECT_ROOT}/test)


# SET (GTEST_ROOT /home/ice/workspace/googletest)
SET (GTEST_ROOT ${TEST_ROOT}/googletest)
SET (GTEST_INCLUDE ${GTEST_ROOT}/googletest/include)
SET (GMOCK_INCLUDE ${GTEST_ROOT}/googlemock/include)


# 引入 googletest 路径
# INCLUDE_DIRECTORIES (AFTER SYSTEM ${GTEST_INCLUDE})
INCLUDE_DIRECTORIES (${GTEST_INCLUDE})
# googletest 库
SET (GTEST_LIB gtest gtest_main)


# 引入公共库路径
# INCLUDE_DIRECTORIES (${COMMON_ROOT}/)
# INCLUDE_DIRECTORIES (${SRC_ROOT}/common)





# 编译程序
ADD_SUBDIRECTORY (${TEST_ROOT}/gtest)



