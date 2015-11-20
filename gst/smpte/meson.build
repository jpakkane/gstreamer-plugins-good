smpte_sources = [
  'gstsmpte.c',
  'gstmask.c',
  'barboxwipes.c',
  'paint.c',
  'gstsmptealpha.c',
  'plugin.c',
]

gstsmpte = library('gstsmpte',
  smpte_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstvideo_dep, gst_dep, libm],
)
