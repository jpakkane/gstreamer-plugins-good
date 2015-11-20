audioparsers_src = [
  'gstaacparse.c',
  'gstamrparse.c',
  'gstac3parse.c',
  'gstdcaparse.c',
  'gstflacparse.c',
  'gstmpegaudioparse.c',
  'gstsbcparse.c',
  'gstwavpackparse.c',
  'plugin.c',
]

gstaudioparsers = library('gstaudioparsers',
  audioparsers_src,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstpbutils_dep, gstaudio_dep, gsttag_dep])
