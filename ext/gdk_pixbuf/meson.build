pixbuf_sources = [
  'gstgdkpixbufdec.c',
  'gstgdkpixbufoverlay.c',
  'gstgdkpixbufplugin.c',
  'gstgdkpixbufsink.c',
]

gstgdkpixbuf = library('gstgdkpixbuf',
  pixbuf_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstvideo_dep, gstcontroller_dep, gdkpixbuf_dep],
)
