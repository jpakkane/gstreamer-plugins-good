dtmf_sources = [
  'gstdtmfsrc.c',
  'gstrtpdtmfsrc.c',
  'gstrtpdtmfdepay.c',
  'gstdtmf.c'
]

gstdtmf = library('gstdtmf',
  dtmf_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstrtp_dep, libm]
)

