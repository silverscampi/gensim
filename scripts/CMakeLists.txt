SET(ARCHSIM_BINARY "${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/archsim")
CONFIGURE_FILE(${CMAKE_CURRENT_SOURCE_DIR}/archsim-armv7a-user.config ${CMAKE_CURRENT_BINARY_DIR}/archsim-armv7a-user)
CONFIGURE_FILE(${CMAKE_CURRENT_SOURCE_DIR}/archsim-x86_64-user.config ${CMAKE_CURRENT_BINARY_DIR}/archsim-x86_64-user)

FILE(
	COPY ${CMAKE_CURRENT_BINARY_DIR}/archsim-armv7a-user
	DESTINATION ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}
	FILE_PERMISSIONS OWNER_READ OWNER_EXECUTE OWNER_WRITE
)

FILE(
	COPY ${CMAKE_CURRENT_BINARY_DIR}/archsim-x86_64-user
	DESTINATION ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}
	FILE_PERMISSIONS OWNER_READ OWNER_EXECUTE OWNER_WRITE
)
