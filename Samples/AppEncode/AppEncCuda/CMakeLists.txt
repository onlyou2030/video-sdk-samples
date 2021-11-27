cmake_minimum_required(VERSION 3.19)
project(AppEncCuda)

include_directories(..)
include_directories(../../NvCodec)

list(APPEND SRC_LIST
	AppEncCuda.cpp
	../../NvCodec/NvEncoder/NvEncoder.cpp
	../../NvCodec/NvEncoder/NvEncoder.h
	../../NvCodec/NvEncoder/NvEncoderCuda.cpp
	../../NvCodec/NvEncoder/NvEncoderCuda.h
	../../NvCodec/NvEncoder/NvEncoder.h
	../../Utils/NvCodecUtils.h
	../../Utils/NvEncoderCLIOptions.h
	../../Utils/Logger.h
)

add_executable(AppEncCuda ${SRC_LIST})