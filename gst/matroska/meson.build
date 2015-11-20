matroska_sources = [
  'ebml-read.c',
  'ebml-write.c',
  'matroska.c',
  'matroska-demux.c',
  'matroska-parse.c',
  'matroska-ids.c',
  'matroska-mux.c',
  'matroska-read-common.c',
  'webm-mux.c',
  'lzo.c',
]


gstmatroska = library('gstmatroska',
  matroska_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, zlib_dep, bz2lib, libm],
)
