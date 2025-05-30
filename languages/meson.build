languages = fs.read('language-code').splitlines()

foreach lang : languages
  lang = lang.split()[0]
  if fs.exists(lang)
    py.install_sources(
      lang / 'faugus-launcher.mo',
      lang / 'faugus-proton-manager.mo',
      lang / 'faugus-run.mo',
      subdir: 'locale' / lang / 'LC_MESSAGES',
    )
  endif
endforeach
