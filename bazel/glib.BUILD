# load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

# configure_make(
#   name = "foreign_glib",
#   autoconf = True,
#   configure_in_place = True,
#   configure_options = [
#     "--silent",
#     "--disable-fam",
#     "--disable-libmount",
#     "--disable-dtrace",
#     "--disable-compile-warnings",
#     "--with-pcre=internal",
#   ],
#   lib_source = "",
# )

# genrule(
#     name = "gen_configure",
#     srcs = [
#         "configure",
#         "config.guess",
#         "config.sub",
#         "install-sh",
#         "ltmain.sh",
#         "missing",
#         "glib/glib.h",
#         "po/LINGUAS",
#     ] + glob(["**/*.in"]),
#     outs = [
#         "config.h",
#         "glibconfig.h",
#     ],
#     cmd = "AR=$(AR) C_COMPILER=$(C_COMPILER) CC=$(CC) NM=$(NM) OBJCOPY=$(OBJCOPY) STRIP=$(STRIP) ./$(location configure) --silent --disable-fam --disable-libmount --disable-dtrace --disable-compile-warnings --with-pcre=internal " +
#           "&& cp --verbose -- config.h $(location config.h)" +
#           "&& cp --verbose -- glib/glibconfig.h $(location glibconfig.h)",
#     toolchains = [
#       "@bazel_tools//tools/cpp:current_cc_toolchain",
#     ],
# )

cc_library(
    name = "charset",
    srcs = [
        "config.h",
        "glib/libcharset/localcharset.c",
    ],
    hdrs = ["glib/libcharset/localcharset.h"],
    copts = [
        "-DHAVE_CONFIG_H",
        "-DLIBDIR='\"/nonexistent\"'",
    ],
)

cc_library(
    name = "glib",
    srcs = [
        "glib/deprecated/gallocator.c",
        "glib/deprecated/gcache.c",
        "glib/deprecated/gcompletion.c",
        "glib/deprecated/grel.c",
        "glib/deprecated/gthread.h",
        "glib/deprecated/gthread-deprecated.c",
        "glib/garray.c",
        "glib/gasyncqueue.c",
        "glib/gasyncqueueprivate.h",
        "glib/gatomic.c",
        "glib/gbacktrace.c",
        "glib/gbase64.c",
        "glib/gbitlock.c",
        "glib/gbookmarkfile.c",
        "glib/gbytes.c",
        "glib/gcharset.c",
        "glib/gcharsetprivate.h",
        "glib/gchecksum.c",
        "glib/gconvert.c",
        "glib/gdataset.c",
        "glib/gdatasetprivate.h",
        "glib/gdate.c",
        "glib/gdatetime.c",
        "glib/gdir.c",
        "glib/genviron.c",
        "glib/gerror.c",
        "glib/gfileutils.c",
        "glib/ggettext.c",
        "glib/ghash.c",
        "glib/ghmac.c",
        "glib/ghook.c",
        "glib/ghostutils.c",
        "glib/giochannel.c",
        "glib/giounix.c",
        "glib/gkeyfile.c",
        "glib/glib-autocleanups.h",
        "glib/glib-init.c",
        "glib/glib-init.h",
        "glib/glib-private.c",
        "glib/glib-unix.c",
        "glib/glist.c",
        "glib/gmain.c",
        "glib/gmain-internal.h",
        "glib/gmappedfile.c",
        "glib/gmarkup.c",
        "glib/gmem.c",
        "glib/gmessages.c",
        "glib/gnode.c",
        "glib/goption.c",
        "glib/gpattern.c",
        "glib/gpoll.c",
        "glib/gprimes.c",
        "glib/gprintf.c",
        "glib/gqsort.c",
        "glib/gquark.c",
        "glib/gqueue.c",
        "glib/grand.c",
        "glib/gregex.c",
        "glib/gscanner.c",
        "glib/gsequence.c",
        "glib/gshell.c",
        "glib/gslice.c",
        "glib/gslist.c",
        "glib/gspawn.c",
        "glib/gstdio.c",
        "glib/gstdioprivate.h",
        "glib/gstrfuncs.c",
        "glib/gstring.c",
        "glib/gstringchunk.c",
        "glib/gtestutils.c",
        "glib/gthread.c",
        "glib/gthread-posix.c",
        "glib/gthreadpool.c",
        "glib/gthreadprivate.h",
        "glib/gtimer.c",
        "glib/gtimezone.c",
        "glib/gtranslit.c",
        "glib/gtranslit-data.h",
        "glib/gtrashstack.c",
        "glib/gtree.c",
        "glib/gunibreak.c",
        "glib/gunibreak.h",
        "glib/gunicodeprivate.h",
        "glib/gunicollate.c",
        "glib/gunidecomp.c",
        "glib/gunidecomp.h",
        "glib/guniprop.c",
        "glib/gurifuncs.c",
        "glib/gutf8.c",
        "glib/gutils.c",
        "glib/guuid.h",
        "glib/gvariant.c",
        "glib/gvariant-core.c",
        "glib/gvariant-core.h",
        "glib/gvariant-internal.h",
        "glib/gvariant-parser.c",
        "glib/gvariant-serialiser.c",
        "glib/gvariant-serialiser.h",
        "glib/gvarianttype.c",
        "glib/gvarianttypeinfo.c",
        "glib/gvarianttypeinfo.h",
        "glib/gversion.c",
        "glib/gwakeup.c",
        "glib/gwakeup.h",
        "glib/libcharset/libcharset.h",
        "glib/pcre/pcre.h",
    ],
    hdrs = [
        "config.h",
        "glib/deprecated/gallocator.h",
        "glib/deprecated/gcache.h",
        "glib/deprecated/gcompletion.h",
        "glib/deprecated/gmain.h",
        "glib/deprecated/grel.h",
        "glib/galloca.h",
        "glib/garray.h",
        "glib/gasyncqueue.h",
        "glib/gatomic.h",
        "glib/gbacktrace.h",
        "glib/gbase64.h",
        "glib/gbitlock.h",
        "glib/gbookmarkfile.h",
        "glib/gbytes.h",
        "glib/gcharset.h",
        "glib/gchecksum.h",
        "glib/gconstructor.h",
        "glib/gconvert.h",
        "glib/gdataset.h",
        "glib/gdate.h",
        "glib/gdatetime.h",
        "glib/gdir.h",
        "glib/genviron.h",
        "glib/gerror.h",
        "glib/gfileutils.h",
        "glib/ggettext.h",
        "glib/ghash.h",
        "glib/ghmac.h",
        "glib/ghook.h",
        "glib/ghostutils.h",
        "glib/giochannel.h",
        "glib/gkeyfile.h",
        "glib/glib.h",
        "glib/glib-private.h",
        "glib/glib-unix.h",
        "glib/glib_trace.h",
        "glib/glibintl.h",
        "glib/glist.h",
        "glib/gmacros.h",
        "glib/gmain.h",
        "glib/gmappedfile.h",
        "glib/gmarkup.h",
        "glib/gmem.h",
        "glib/gmessages.h",
        "glib/gmirroringtable.h",
        "glib/gnode.h",
        "glib/goption.h",
        "glib/gpattern.h",
        "glib/gpoll.h",
        "glib/gprimes.h",
        "glib/gprintf.h",
        "glib/gprintfint.h",
        "glib/gqsort.h",
        "glib/gquark.h",
        "glib/gqueue.h",
        "glib/grand.h",
        "glib/gregex.h",
        "glib/gscanner.h",
        "glib/gscripttable.h",
        "glib/gsequence.h",
        "glib/gshell.h",
        "glib/gslice.h",
        "glib/gslist.h",
        "glib/gspawn.h",
        "glib/gstdio.h",
        "glib/gstrfuncs.h",
        "glib/gstring.h",
        "glib/gstringchunk.h",
        "glib/gtestutils.h",
        "glib/gthread.h",
        "glib/gthreadpool.h",
        "glib/gtimer.h",
        "glib/gtimezone.h",
        "glib/gtrashstack.h",
        "glib/gtree.h",
        "glib/gtypes.h",
        "glib/gunichartables.h",
        "glib/gunicode.h",
        "glib/gunicomp.h",
        "glib/gurifuncs.h",
        "glib/gutils.h",
        "glib/gvariant.h",
        "glib/gvarianttype.h",
        "glib/gversion.h",
        "glib/gversionmacros.h",
        "glib/valgrind.h",
        "glibconfig.h",
    ],
    copts = [
        "-Iexternal/glib_archive/glib",
        "-DGLIB_COMPILATION",
        "-DG_DISABLE_CAST_CHECKS",
        "-DG_LOG_DOMAIN='\"GLib\"'",
        "-DHAVE_CONFIG_H",
        "-DPCRE_STATIC",
    ],
    includes = ["."],
    visibility = ["//visibility:public"],
    deps = [":charset"],
)
