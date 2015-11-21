jpeg_sources = [
  'gstjpeg.c',
  'gstjpegenc.c',
  'gstjpegdec.c',
]

gstjpeg = library('gstjpeg',
  jpeg_sources,
  c_args : core_args,
  include_directories : core_incs,
  dependencies : [gstbase_dep, gstvideo_dep, jpeglib, libm],
)
