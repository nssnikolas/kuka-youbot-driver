cmake_minimum_required(VERSION 2.8)

add_executable(base_arm_gripper_test
  TestSuite.cpp
  YouBotBaseTest.cpp
  YouBotBaseTestWithoutThread.cpp
  YouBotBaseKinematicsTest.cpp
  YouBotArmTest.cpp
  YouBotArmTestWithoutThread.cpp
  YouBotGripperTest.cpp
)

target_link_libraries(base_arm_gripper_test YouBotDriver cppunit)

install(TARGETS base_arm_gripper_test
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
)
