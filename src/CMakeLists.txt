cmake_minimum_required(VERSION 3.10)

project(candle_api)

add_library(candle_api SHARED
	candle.c
	candle_ctrl_req.c
)

add_definitions(-DCANDLE_API_LIBRARY -DUNICODE -DNTDDI_VERSION=NTDDI_VISTA -D_WIN32_WINNT=_WIN32_WINNT_VISTA)

set_target_properties(candle_api PROPERTIES PREFIX "")

target_link_libraries(candle_api
	SetupApi
	winusb
	Ole32
)