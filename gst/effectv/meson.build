effect_sources = [
  'gsteffectv.c', 'gstedge.c', 'gstaging.c', 'gstdice.c', 'gstwarp.c',
  'gstshagadelic.c', 'gstvertigo.c', 'gstrev.c', 'gstquark.c', 'gstop.c',
  'gstradioac.c', 'gststreak.c', 'gstripple.c'
]

gsteffectv = library('gsteffectv',
  effect_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstvideo_dep, libm]
)
