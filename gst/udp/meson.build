udp_sources = [
  'gstudp.c',
  'gstudpsrc.c',
  'gstudpsink.c',
  'gstmultiudpsink.c',
  'gstdynudpsink.c',
  'gstudpnetutils.c'
]

gstudp = library('gstudp',
  udp_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstnet_dep, gio_dep],
)
