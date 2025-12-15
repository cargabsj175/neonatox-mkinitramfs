project(
  'mkinitramfs',
  'c',
  version : '1.0.0',
  meson_version : '>= 0.56'
)

# No compilamos nada, solo instalamos scripts
# Usamos 'c' solo para que Meson no proteste

sbindir = get_option('sbindir')
datadir = get_option('datadir')
docdir  = join_paths(datadir, 'doc', 'mkinitramfs')

# Script principal
install_data(
  'src/mkinitramfs',
  install_dir : sbindir,
  install_mode : 'rwxr-xr-x'
)

# init del initramfs
install_data(
  'data/init.in',
  install_dir : join_paths(datadir, 'mkinitramfs'),
  install_mode : 'rwxr-xr-x'
)

# Documentación
install_data(
  'README.html',
  install_dir : docdir
)
