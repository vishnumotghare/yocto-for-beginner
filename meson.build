project('yocto-docbook', 'c', 'cpp',
  version: '1.0.0',
  meson_version : '>= 0.49.2',
  default_options : [
    'buildtype=debugoptimized',
    'warning_level=1',
    'c_std=gnu99'
  ]
)

# Dependencies
glib_dep = dependency('glib-2.0')
gio_dep = dependency('gio-2.0')

gnome = import('gnome')
subdir('docs')
