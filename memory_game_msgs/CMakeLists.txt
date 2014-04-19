cmake_minimum_required(VERSION 2.8.3)
project(memory_game_msgs)

find_package(catkin REQUIRED COMPONENTS 
    message_generation 
    std_msgs 
    geometry_msgs
)

add_message_files(
  FILES
  MemoryCard.msg
  MemoryCardArray.msg
  MemoryHeadControl.msg
)

# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES strands_perception_people_msgs
#  CATKIN_DEPENDS message_generation std_msgs
#  DEPENDS system_lib
)
