cmake_minimum_required(VERSION 2.8.3)
project(industrial_ci_testpkg)

find_package(catkin REQUIRED COMPONENTS rospy_tutorials rostest)

catkin_package()

if (CATKIN_ENABLE_TESTING)
  add_rostest(test/example_ros.test)
endif()

install(DIRECTORY test DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
