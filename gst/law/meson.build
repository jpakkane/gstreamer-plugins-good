gstalaw = library('gstalaw',
  'alaw-encode.c', 'alaw-decode.c', 'alaw.c',
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstaudio_dep]
)

gstmulaw = library('gstmulaw',
  'mulaw-encode.c', 'mulaw-conversion.c', 'mulaw-decode.c', 'mulaw.c',
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstaudio_dep]
)
