project('gst-plugins-good', 'c', 'cpp', version : '1.4.5',
  default_options : ['warning_level=1', 'c_std=gnu99'])

version_str = meson.project_version()
varr = version_str.split('.')
version_major = varr[0]
version_minor = varr[1]
version_micro = varr[2]
version_nano = 1
api_version = '1.0'

cc = meson.get_compiler('c')
cdata = configuration_data()
check_headers = [
  ['HAVE_DLFCN_H', 'dlfcn.h'],
  ['HAVE_FCNTL_H', 'fcntl.h'],
  ['HAVE_INTTYPES_H', 'inttypes.h'],
  ['HAVE_MEMORY_H', 'memory.h'],
  ['HAVE_PROCESS_H', 'process.h'],
  ['HAVE_STDINT_H', 'stdint.h'],
  ['HAVE_STDLIB_H', 'stdlib.h'],
  ['HAVE_STRINGS_H', 'strings.h'],
  ['HAVE_STRING_H', 'string.h'],
  ['HAVE_SYS_IOCTL_H', 'sys/ioctl.h'],
  ['HAVE_SYS_PARAM_H', 'sys/param.h'],
  ['HAVE_SYS_SOCKET_H', 'sys/socket.h'],
  ['HAVE_SYS_STAT_H', 'sys/stat.h'],
  ['HAVE_SYS_TIME_H', 'sys/time.h'],
  ['HAVE_SYS_TYPES_H', 'sys/types.h'],
  ['HAVE_UNISTD_H', 'unistd.h'],
]

foreach h : check_headers
  if cc.has_header(h.get(1))
    cdata.set(h.get(0), 1)
  endif
endforeach

check_functions = [
# check token HAVE_AALIB
  ['HAVE_ASINH', 'asinh', '#include<math.h>'],
# check token HAVE_BZ2
# check token HAVE_CFLOCALECOPYCURRENT
# check token HAVE_CFPREFERENCESCOPYAPPVALUE
  ['HAVE_CLOCK_GETTIME', 'clock_gettime', '#include<time.h>'],
  ['HAVE_COSH', 'cosh', '#include<math.h>'],
# check token HAVE_CPU_ALPHA
# check token HAVE_CPU_ARM
# check token HAVE_CPU_CRIS
# check token HAVE_CPU_CRISV32
# check token HAVE_CPU_HPPA
# check token HAVE_CPU_I386
# check token HAVE_CPU_IA64
# check token HAVE_CPU_M68K
# check token HAVE_CPU_MIPS
# check token HAVE_CPU_PPC
# check token HAVE_CPU_PPC64
# check token HAVE_CPU_S390
# check token HAVE_CPU_SPARC
# check token HAVE_CPU_X86_64
  ['HAVE_DCGETTEXT', 'dcgettext', '#include<libintl.h>'],
# check token HAVE_DIRECTSOUND
# check token HAVE_DOWHILE_MACROS
# check token HAVE_DV1394
# check token HAVE_EXPERIMENTAL
# check token HAVE_EXTERNAL
# check token HAVE_FIONREAD_IN_SYS_FILIO
# check token HAVE_FIONREAD_IN_SYS_IOCTL
# check token HAVE_FLAC
# check token HAVE_FPCLASS
# check token HAVE_GCC_ASM
# check token HAVE_GDK_PIXBUF
  ['HAVE_GETPAGESIZE', 'getpagesize', '#include<unistd.h>'],
# check token HAVE_GETTEXT
# check token HAVE_GST_V4L2
# check token HAVE_GUDEV
# check token HAVE_ICONV
# check token HAVE_IOS
# check token HAVE_IP_MREQN
  ['HAVE_ISINF', 'isinf', '#include<math.h>'],
# check token HAVE_JACK
# check token HAVE_JACK_0_120_1
# check token HAVE_JACK_1_9_7
# check token HAVE_JPEG
# check token HAVE_LIBCACA
# check token HAVE_LIBDV
# check token HAVE_LIBPNG
# check token HAVE_LIBV4L2
  ['HAVE_MMAP', 'mmap', '#include<sys/mman.h>'],
# check token HAVE_ORC
# check token HAVE_OSS
# check token HAVE_OSS4
# check token HAVE_OSS_INCLUDE_IN_MACHINE
# check token HAVE_OSS_INCLUDE_IN_ROOT
# check token HAVE_OSS_INCLUDE_IN_SYS
# check token HAVE_OSX_AUDIO
# check token HAVE_OSX_VIDEO
# check token HAVE_PULSE
# check token HAVE_RDTSC
# check token HAVE_RINT
# check token HAVE_SHOUT2
  ['HAVE_SINH', 'sinh', '#include<math.h>'],
# check token HAVE_SOUP
# check token HAVE_SPEEX
# check token HAVE_SUNAUDIO
# check token HAVE_TAGLIB
# check token HAVE_VALGRIND
# check token HAVE_VP8_DECODER
# check token HAVE_VP8_ENCODER
# check token HAVE_VP9_DECODER
# check token HAVE_VP9_ENCODER
# check token HAVE_VPX
# check token HAVE_WAVEFORM
# check token HAVE_WAVPACK
# check token HAVE_X
# check token HAVE_XSHM
# check token HAVE_ZLIB
]

foreach f : check_functions
  if cc.has_function(f.get(1), prefix : f.get(2))
    cdata.set(f.get(0), 1)
  endif
endforeach

cdata.set('SIZEOF_CHAR', cc.sizeof('char'))
cdata.set('SIZEOF_INT', cc.sizeof('int'))
cdata.set('SIZEOF_LONG', cc.sizeof('long'))
cdata.set('SIZEOF_SHORT', cc.sizeof('short'))
cdata.set('SIZEOF_VOIDP', cc.sizeof('void*'))

# Here be fixmes.
cdata.set('HAVE_CPU_X86_64', 1)
cdata.set('HAVE_GCC_ASM', 1)
cdata.set('VERSION', '"@0@"'.format(version_str))
cdata.set('PACKAGE_VERSION', '"@0@"'.format(version_str))
cdata.set('GST_LICENSE', '"FIXME"')
cdata.set('PACKAGE', '"FIXME"')
cdata.set('GETTEXT_PACKAGE', '"FIXME"')
cdata.set('GST_PACKAGE_NAME', '"FIXME"')
cdata.set('GST_PACKAGE_ORIGIN', '"FIXME"')

# Mandatory GST deps
gst_dep = dependency('gstreamer-1.0')
gstvideo_dep = dependency('gstreamer-video-1.0')
gstpbutils_dep = dependency('gstreamer-pbutils-1.0')
gsttag_dep = dependency('gstreamer-tag-1.0')
gstfft_dep = dependency('gstreamer-fft-1.0')
gstaudio_dep = dependency('gstreamer-audio-1.0')
gstbase_dep = dependency('gstreamer-base-1.0')
gstriff_dep = dependency('gstreamer-riff-1.0')
gstrtp_dep = dependency('gstreamer-rtp-1.0')
gstnet_dep = dependency('gstreamer-net-1.0')
gstsdp_dep = dependency('gstreamer-sdp-1.0')
gstrtsp_dep = dependency('gstreamer-rtsp-1.0')

orc_dep = dependency('orc-0.4')
zlib_dep = dependency('zlib')
bz2lib = find_library('bz2', required : false)
gio_dep = dependency('gio-2.0')

x_dep = dependency('x11', required : false)
xfixes_dep = dependency('xfixes', required : false)
xdamage_dep = dependency('xdamage', required : false)

libm = find_library('m', required : false)

if bz2lib.found()
  cdata.set('HAVE_BZ2', 1)
endif

# Check all of the things.
deps = [
  ['gtk_dep','gtk+-3.0', '', ''],
  ['gtkx_dep','gtk+-x11-3.0', '', ''],
  ['gudev_dep','gudev-1.0', '>=147', ''],
  ['libv4l2_dep','libv4l2', '', ''],
  ['xfixes_dep','xfixes', '', ''],
  ['xdamage_dep','xdamage', '', ''],
  ['cairo_dep','cairo', '>=1.10.0', ''],
  ['flac_dep','flac', '>=1.1.4', 'HAVE_FLAC'],
  ['gdkpixbuf_dep','gdk-pixbuf-2.0', '>=2.8.0', ''],
  ['jack_dep','jack', '>=1.9.7', 'HAVE_JACK_1_9_7'],
  ['caca_dep','caca', '', ''],
  ['libdv_dep','libdv', '>=0.100', ''],
  ['libpng_dep','libpng', '>=1.2', ''],
  ['libpulse_dep','libpulse', '>=2.0', 'HAVE_PULSE'],
  ['libraw1394_dep','libraw1394', '>=2.0.0', ''],
  ['libiec61883_dep','libiec61883', '>=1.0.0', ''],
  ['libraw1394_dep','libraw1394', '>=1.1.0', ''],
  ['shout_dep','shout', '>=2.0', ''],
  ['libsoup_dep','libsoup-2.4', '>=2.40', ''],
  ['speex_dep','speex', '>=1.1.6', ''],
  ['taglib_dep','taglib', '>=1.5', ''],
  ['vpx_dep','vpx', '>=1.3.0', 'HAVE_VPX'],
  ['wavpack_dep','wavpack', '>= 4.20', 'HAVE_WAVPACK'],
]

foreach d : deps
  varname = d[0]
  depname = d[1]
  version = d[2]
  confhname = d[3]
  if version == ''
    curdep = dependency(depname, required : false)
  else
    curdep = dependency(depname, required : false, version : version)
  endif
  set_variable(varname, curdep)
  if curdep.found() and confhname != ''
    cdata.set(confhname, 1)
  endif
endforeach

configure_file(input : 'config.h.meson',
  output : 'config.h',
  configuration : cdata)

core_args = ['-DHAVE_CONFIG_H']
core_incs = include_directories('.', 'gst-libs')

subdir('gst')
subdir('sys')
