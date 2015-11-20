vfilter_sources = [
  'plugin.c',
  'gstvideoflip.c',
  'gstvideobalance.c',
  'gstgamma.c',
  'gstvideomedian.c',
]

gstvideofilter = library('gstvideofilter',
  vfilter_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstvideo_dep],
)
