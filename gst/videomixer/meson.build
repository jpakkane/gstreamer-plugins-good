vmixer_sources = [
  'blend.c',
  'videoconvert.c',
  'gstcms.c',
  'videomixer2.c',
]

vmix_c = configure_file(input : 'videomixerorc-dist.c',
  output : 'videomixerorc.c',
  configuration : configuration_data()
)

vmix_h = configure_file(input : 'videomixerorc-dist.h',
  output : 'videomixerorc.h',
  configuration : configuration_data()
)


gstvideomixer = library('gstvideomixer',
  vmixer_sources, vmix_c,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [orc_dep, gstvideo_dep, gstbase_dep, libm],
)
