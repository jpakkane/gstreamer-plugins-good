png_sources = [
  'gstpng.c',
  'gstpngenc.c',
  'gstpngdec.c',
]

gstpng = library('gstpng',
  png_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstvideo_dep, libpng_dep],
)
