noinst_PROGRAMS = server-alsasrc-PCMA client-PCMA \
	client-rtpaux server-rtpaux

# FIXME 0.11: ignore GValueArray warnings for now until this is sorted
ERROR_CFLAGS=

server_rtpaux_SOURCES = server-rtpaux.c
server_rtpaux_CFLAGS = $(GST_CFLAGS)
server_rtpaux_LDADD = $(GST_LIBS)

client_rtpaux_SOURCES = client-rtpaux.c
client_rtpaux_CFLAGS = $(GST_CFLAGS)
client_rtpaux_LDADD = $(GST_LIBS)

server_alsasrc_PCMA_SOURCES = server-alsasrc-PCMA.c
server_alsasrc_PCMA_CFLAGS = $(GST_CFLAGS)
server_alsasrc_PCMA_LDADD = $(GST_LIBS) $(LIBM)

client_PCMA_SOURCES = client-PCMA.c
client_PCMA_CFLAGS = $(GST_CFLAGS)
client_PCMA_LDADD = $(GST_LIBS) $(LIBM)

noinst_SCRIPTS=client-H263p-AMR.sh \
               client-H263p-PCMA.sh \
               client-H264-PCMA.sh \
               client-PCMA.sh \
               server-alsasrc-PCMA.sh \
               server-v4l2-H263p-alsasrc-AMR.sh \
               server-v4l2-H264-alsasrc-PCMA.sh \
               server-VTS-H263p-ATS-PCMA.sh

EXTRA_DIST= $(noinst_SCRIPTS) \
	    client-H263p-PCMA.sdp \
            client-H264-PCMA.sdp
