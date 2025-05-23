# Aseprite Document Library
# Copyright (C) 2019-2024 Igara Studio S.A.
# Copyright (C) 2001-2018 David Capello

if(WIN32)
  add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

add_library(doc-lib
  algo.cpp
  algorithm/fill_selection.cpp
  algorithm/flip_image.cpp
  algorithm/floodfill.cpp
  algorithm/modify_selection.cpp
  algorithm/polygon.cpp
  algorithm/random_image.cpp
  algorithm/resize_image.cpp
  algorithm/rotate.cpp
  algorithm/rotsprite.cpp
  algorithm/shift_image.cpp
  algorithm/shrink_bounds.cpp
  algorithm/stroke_selection.cpp
  anidir.cpp
  blend_funcs.cpp
  blend_image.cpp
  blend_mode.cpp
  brush.cpp
  brush_type.cpp
  cel.cpp
  cel_data.cpp
  cel_data_io.cpp
  cel_io.cpp
  cels_range.cpp
  color.cpp
  compressed_image.cpp
  document.cpp
  file/act_file.cpp
  file/col_file.cpp
  file/gpl_file.cpp
  file/hex_file.cpp
  file/pal_file.cpp
  frames_sequence.cpp
  grid.cpp
  grid_io.cpp
  image.cpp
  image_impl.cpp
  image_io.cpp
  layer.cpp
  layer_io.cpp
  layer_list.cpp
  layer_tilemap.cpp
  mask.cpp
  mask_boundaries.cpp
  mask_io.cpp
  object.cpp
  object.cpp
  octree_map.cpp
  palette.cpp
  palette_io.cpp
  playback.cpp
  primitives.cpp
  remap.cpp
  render_plan.cpp
  rgbmap_base.cpp
  rgbmap_rgb5a3.cpp
  selected_frames.cpp
  selected_layers.cpp
  slice.cpp
  slice_io.cpp
  slices.cpp
  sort_palette.cpp
  sprite.cpp
  sprites.cpp
  string_io.cpp
  subobjects_io.cpp
  tag.cpp
  tag_io.cpp
  tags.cpp
  tile_primitives.cpp
  tileset.cpp
  tileset_io.cpp
  tilesets.cpp
  user_data.cpp
  user_data_io.cpp
  util.cpp
  uuid_io.cpp)

target_link_libraries(doc-lib
  laf-gfx
  laf-base
  fixmath-lib
  cityhash)

target_include_directories(doc-lib
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/..)
