audiofx_sources = [
  'audiofx.c',
  'audiopanorama.c',
  'audioinvert.c',
  'audioamplify.c',
  'audiodynamic.c',
  'audiokaraoke.c',
  'audiofxbaseiirfilter.c',
  'audiocheblimit.c',
  'audiochebband.c',
  'audioiirfilter.c',
  'audiofxbasefirfilter.c',
  'audiowsincband.c',
  'audiowsinclimit.c',
  'audiofirfilter.c',
  'audioecho.c',
  'gstscaletempo.c'
]

pano_c = configure_file(input : 'audiopanoramaorc-dist.c',
  output : 'audiopanoramaorc.c',
  configuration : configuration_data()
)

pano_h = configure_file(input : 'audiopanoramaorc-dist.h',
  output : 'audiopanoramaorc.h',
  configuration : configuration_data()
)

gstaudiofx = library('gstaudiofx',
  audiofx_sources, #pano_c,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstaudio_dep, gstfft_dep]
)
