vpx_sources = [
  'gstvp8dec.c',
  'gstvp8enc.c',
  'gstvp8utils.c',
  'gstvp9dec.c',
  'gstvp9enc.c',
  'plugin.c',
]

vpx_args = ['-DGST_USE_UNSTABLE_API']

gstvpx = library('gstvpx',
  vpx_sources,
  c_args : core_args + vpx_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gsttag_dep, gstvideo_dep, vpx_dep],
)

