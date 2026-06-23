add_custom_target(samples)

add_executable(maze maze.c)
target_link_libraries(maze 
    PRIVATE
        cli
        random
        str_view::str_view
        ccc::ccc
        std_allocator
        defer
)
add_dependencies(samples maze)

add_executable(graph graph.c)
target_link_libraries(graph 
    PRIVATE
        cli
        random
        str_view::str_view
        ccc::ccc
        std_allocator
        defer
)
add_dependencies(samples graph)

add_executable(words words.c)
target_link_libraries(words 
    PRIVATE
        cli
        str_view::str_view
        ccc::ccc
        std_allocator
        string_arena
        defer
)
add_dependencies(samples words)

add_executable(ccczip ccczip.c)
target_link_libraries(ccczip 
    PRIVATE
        cli
        str_view::str_view
        ccc::ccc
        std_allocator
        string_arena
        defer
)
add_dependencies(samples ccczip)
