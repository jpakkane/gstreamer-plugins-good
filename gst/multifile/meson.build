multifile_sources = [
  'gstmultifilesink.c',
  'gstmultifilesrc.c',
  'gstmultifile.c',
  'gstsplitfilesrc.c',
  'patternspec.c',
]

gstmultifile = library('gstmultifile',
  multifile_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gio_dep],
)

