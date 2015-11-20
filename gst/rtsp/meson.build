rtsp_sources = [
  'gstrtsp.c',
  'gstrtspsrc.c',
  'gstrtpdec.c',
  'gstrtspext.c',
]

gstrtsp = library('gstrtsp',
  rtsp_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gio_dep, gstrtp_dep, gstrtsp_dep, gstsdp_dep, gstnet_dep],
)
