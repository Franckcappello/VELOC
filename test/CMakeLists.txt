# Comment as needed to reduce build time
add_executable (heatdis_original heatdis_original.c)
add_executable (heatdis_mem heatdis_mem.c)
add_executable (heatdis_file heatdis_file.c)

# Link the executable to the necessary libraries.
target_link_libraries (heatdis_original ${MPI_C_LIBRARIES} m)
target_link_libraries (heatdis_mem ${MPI_C_LIBRARIES} m veloc-client)
target_link_libraries (heatdis_file ${MPI_C_LIBRARIES} m veloc-client)
