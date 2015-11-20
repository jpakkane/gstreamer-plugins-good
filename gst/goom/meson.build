goom_sources = [
  'gstgoom.c',
  'drawmethods.c',
  'sound_tester.c',
  'mathtools.c',
  'lines.c',
  'ifs.c',
  'surf3d.c',
  'tentacle3d.c',
  'v3d.c',
  'convolve_fx.c',
  'flying_stars_fx.c',
  'plugin_info.c',
  'goom_tools.c',
  'config_param.c',
  'filters.c',
  'goom_core.c',
  'graphic.c',
]


gstgoom = library('gstgoom',
  goom_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, orc_dep, libm]
)
