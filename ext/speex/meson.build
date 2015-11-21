speex_sources =[
  'gstspeex.c',
  'gstspeexdec.c',
  'gstspeexenc.c',
]

gstspeex = library('gstspeex',
  speex_sources,
  c_args : core_args + ['-DGST_USE_UNSTABLE_API'],
  include_directories : core_incs,
  dependencies : [gstbase_dep, gsttag_dep, gstaudio_dep, speex_dep],
)
