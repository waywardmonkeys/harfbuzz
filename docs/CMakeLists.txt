find_package(GtkDoc 1.25 REQUIRED)

gtk_doc_add_module(
    harfbuzz
    XML harfbuzz-docs.xml
    SOURCE ${CMAKE_SOURCE_DIR}/src
    LIBRARIES harfbuzz
)
add_custom_target(all-documentation ALL)
add_dependencies(all-documentation doc-harfbuzz)
