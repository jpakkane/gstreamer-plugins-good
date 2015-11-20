autodetect_sources = [
  'gstautoaudiosink.c',
  'gstautoaudiosrc.c',
  'gstautodetect.c',
  'gstautovideosink.c',
  'gstautovideosrc.c',
]

gstautodetect = library('gstautodetect',
  autodetect_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gst_dep]
)
