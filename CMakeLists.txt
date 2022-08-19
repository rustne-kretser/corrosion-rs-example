cmake_minimum_required(VERSION 3.15)
project(MyCoolProject LANGUAGES C)

find_package(Corrosion REQUIRED)

corrosion_import_crate(MANIFEST_PATH rust-lib/Cargo.toml)

add_executable(hello main.c)
target_link_libraries(hello PUBLIC rust-lib)
