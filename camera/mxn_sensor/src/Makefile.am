MAIN_TARGET_NAME        = mxn_sensor_arm
DSP_HEADERS_DIR         = $(srcdir)/../../../../trik-media-sensors-dsp/trik/camera/mxn_sensor/

AM_CPPFLAGS             = -I$(DSP_HEADERS_DIR) -I$(srcdir)/../include -Wall -Wextra
AM_CXXFLAGS             = -Weffc++

bin_PROGRAMS            = $(MAIN_TARGET_NAME)

mxn_sensor_arm_SOURCES = main.c \
                         module_ce.c \
                         module_fb.c \
                         module_rc.c \
                         module_v4l2.c \
                         runtime.c \
                         thread_input.c \
                         thread_video.c


#TESTS			= test-xxx
#noinst_PROGRAMS		= $(TESTS)
#SOURCES			= $(top_srcdir)/tests/test.h
#test_xxx_SOURCES	= $(SOURCES) $(top_srcdir)/tests/test_xxx.c

