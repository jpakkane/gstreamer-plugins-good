rtpmanager_sources = [
  'gstrtpmanager.c',
  'gstrtpbin.c',
  'gstrtpdtmfmux.c',
  'gstrtpjitterbuffer.c',
  'gstrtpmux.c',
  'gstrtpptdemux.c',
  'gstrtprtxqueue.c',
  'gstrtprtxreceive.c',
  'gstrtprtxsend.c',
  'gstrtpssrcdemux.c',
  'rtpjitterbuffer.c',
  'rtpsession.c',
  'rtpsource.c',
  'rtpstats.c',
  'gstrtpsession.c',
]

gstrtpmanager = library('gstrtpmanager',
  rtpmanager_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstnet_dep, gstrtp_dep],
)
