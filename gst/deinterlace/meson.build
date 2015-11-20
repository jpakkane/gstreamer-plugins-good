interlace_sources = [
  'gstdeinterlace.c',
  'gstdeinterlacemethod.c',
  'tvtime/tomsmocomp.c',
  'tvtime/greedy.c',
  'tvtime/greedyh.c',
  'tvtime/vfir.c',
  'tvtime/weavetff.c',
  'tvtime/weavebff.c',
  'tvtime/weave.c',
  'tvtime/linear.c',
  'tvtime/linearblend.c',
  'tvtime/scalerbob.c'
]

tvtime_c = configure_file(input : 'tvtime-dist.c',
  output : 'tvtime.c',
  configuration : configuration_data()
)

tvtime_h = configure_file(input : 'tvtime-dist.h',
  output : 'tvtime.h',
  configuration : configuration_data()
)



gstdeinterlace = library('gstdeinterlace',
  interlace_sources, tvtime_c,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [orc_dep, gstbase_dep, gstvideo_dep],
)

