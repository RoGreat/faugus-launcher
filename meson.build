project(
  'faugus-launcher',
  version: '1.5.10.dev0',
  meson_version: '>=1.2.0',
  license: 'MIT',
  license_files: 'LICENSE',
)

py = import('python').find_installation()
fs = import('fs')
gnome = import ('gnome')

subdir('assets')
subdir('languages')

py.install_sources(
  'faugus_launcher.py',
  'faugus_run.py',
  'faugus_proton_manager.py',
  'faugus_components.py',
)

py.install_sources(
  'faugus-launcher.desktop',
  'faugus-shortcut.desktop',
  'faugus-run.desktop',
  'faugus-proton-manager.desktop',
  subdir: 'share' / 'applications',
)

py.install_sources(
  'LICENSE',
  subdir: 'share' / 'licenses' / meson.project_name(),
)

gnome.post_install(
  gtk_update_icon_cache: true
)
