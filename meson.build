project(
  'faugus-launcher',
  version: '1.5.8.dev0',
  meson_version: '>=1.2.0',
  license: 'MIT',
  license_files: 'LICENSE',
)

py = import('python').find_installation()
fs = import('fs')

subdir('assets')
subdir('languages')

py.install_sources(
  'faugus_launcher.py',
  'faugus_run.py',
  'faugus_proton_manager.py',
  'faugus_components.py',
  'faugus_gamepad.py',
)

install_data(
  'faugus-session',
  install_dir: get_option('bindir'),
)

install_data(
  'faugus-launcher.desktop',
  'faugus-shortcut.desktop',
  'faugus-run.desktop',
  'faugus-proton-manager.desktop',
  install_dir: get_option('datadir') / 'share' / 'applications',
)

install_data(
  'faugus-session.desktop',
  install_dir: get_option('datadir') / 'share' / 'wayland-sessions',
)

install_data(
  'LICENSE',
  install_dir: get_option('datadir') / 'share' / 'licenses' / meson.project_name(),
)
