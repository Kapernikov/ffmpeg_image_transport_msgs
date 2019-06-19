cmake_minimum_required(VERSION 3.5)
project(ffmpeg_image_transport_msgs)

# find dependencies
find_package(ament_cmake REQUIRED)
# uncomment the following section in order to fill in
# further dependencies manually.
# find_package(<dependency> REQUIRED)

find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(shape_msgs REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(builtin_interfaces REQUIRED)


rosidl_generate_interfaces(
    ${PROJECT_NAME}
    msg/FFMPEGPacket.msg
    DEPENDENCIES std_msgs
)

ament_export_dependencies(rosidl_default_runtime)


ament_package()

