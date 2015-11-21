soup_sources = [
  'gstsouphttpsrc.c',
  'gstsouphttpclientsink.c',
  'gstsouputils.c',
  'gstsoup.c',
]

soup_args = [
  '-DSOUP_VERSION_MIN_REQUIRED=SOUP_VERSION_2_26',
  '-DSOUP_VERSION_MAX_ALLOWED=SOUP_DEPRECATED_IN_2_26',
]

gstsouphttpsrc = library('gstsouphttpsrc',
  soup_sources,
  c_args : core_args + soup_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gsttag_dep, libsoup_dep],
)
