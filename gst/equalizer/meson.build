eq_sources = [
  'gstiirequalizer.c',
  'gstiirequalizernbands.c',
  'gstiirequalizer3bands.c',
  'gstiirequalizer10bands.c',
]

gstequalizer = library('gstequalizer',
  eq_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstaudio_dep, libm]
)
