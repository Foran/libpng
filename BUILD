genrule(
  name='pnglibconf',
  srcs=[
    '//scripts:pnglibconf_prebuilt',
  ],
  outs=[
    'pnglibconf.h',
  ],
  cmd='cp $(locations //scripts:pnglibconf_prebuilt) $@',
)

cc_library(
  name='libpng',
  srcs=[
    'png.c',
    'pngerror.c',
    'pngget.c',
    'pngmem.c',
    'pngpread.c',
    'pngread.c',
    'pngrio.c',
    'pngrtran.c',
    'pngrutil.c',
    'pngset.c',
    'pngtrans.c',
    'pngwio.c',
    'pngwtran.c',
    'pngwrite.c',
    'pngwutil.c',
    'pngconf.h',
    'pngdebug.h',
    'pnginfo.h',
    'pngpriv.h',
    'pngstruct.h',
    ':pnglibconf',
  ],
  hdrs=[
    'png.h',
  ],
  deps=[
    '@com_github_foran_zlib//:zlib',
  ],
  visibility=['//visibility:public',],
)

cc_binary(
  name='pngtest',
  srcs=[
    'pngtest.c',
  ],
  data=[
    'pngtest.png',
  ],
  deps=[
    ':libpng',
  ],
)

