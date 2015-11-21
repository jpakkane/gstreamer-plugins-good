flac_sources = [
  'gstflac.c',
  'gstflacdec.c',
  'gstflacenc.c',
  'gstflactag.c',
]

gstflac = library('gstflac',
  flac_sources,
  c_args : core_args + ['-DGST_USE_UNSTABLE_API'],
  include_directories : core_incs,
  dependencies : [gstbase_dep, gsttag_dep, gstaudio_dep, flac_dep],
)
