mp4_sources = [
  'isomp4-plugin.c',
  'gstrtpxqtdepay.c',
  'qtdemux.c',
  'qtdemux_types.c',
  'qtdemux_dump.c',
  'qtdemux_lang.c',
  'gstqtmux.c',
  'gstqtmoovrecover.c',
  'atoms.c',
  'atomsrecovery.c',
  'descriptors.c',
  'properties.c',
  'gstqtmuxmap.c'
]

gstisomp4 = library('gstisomp4',
  mp4_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gst_dep, gstriff_dep, gstaudio_dep, gstvideo_dep, gstrtp_dep, gsttag_dep, gstpbutils_dep]
)
