vbox_c = configure_file(input : 'gstvideoboxorc-dist.c',
  output : 'gstvideoboxorc.c',
  configuration : configuration_data()
)

vbox_h = configure_file(input : 'gstvideoboxorc-dist.h',
  output : 'gstvideoboxorc.h',
  configuration : configuration_data()
)

gstvideobox = library('gstvideobox',
  'gstvideobox.c',
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [orc_dep, gstbase_dep, gstvideo_dep],
)
