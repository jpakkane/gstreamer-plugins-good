replaygain_sources = [
  'gstrganalysis.c',
  'gstrglimiter.c',
  'gstrgvolume.c',
  'replaygain.c',
  'rganalysis.c',
]

gstreplaygain = library('gstreplaygain',
  replaygain_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstpbutils_dep, gstaudio_dep, libm],
)

