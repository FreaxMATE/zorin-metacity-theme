install_flavours = []
available_flavours = ['ZorinBlue-Light', 'ZorinBlue-Dark',
                      'ZorinGrey-Light', 'ZorinGrey-Dark',
                      'ZorinGreen-Light', 'ZorinGreen-Dark',
                      'ZorinOrange-Light', 'ZorinOrange-Dark',
                      'ZorinPurple-Light', 'ZorinPurple-Dark',
                      'ZorinRed-Light', 'ZorinRed-Dark'
]

foreach flavour: available_flavours
  if not get_option(flavour)
    message('skip flavour ' + flavour)
    continue
  endif
  install_flavours += flavour
endforeach

foreach flavour: install_flavours
  theme_dir = join_paths(get_option('datadir'), 'themes', flavour)
  install_subdir(join_paths(flavour, 'metacity-1'), install_dir : theme_dir)
endforeach

