avi_sources = [
  'gstavi.c',
  'gstavimux.c',
  'gstavidemux.c',
  'gstavisubtitle.c'
]

gstavi = library('gstavi',
  avi_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gst_dep, gstriff_dep, gstaudio_dep, gstvideo_dep, gsttag_dep]
)
