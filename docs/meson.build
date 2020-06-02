# Check for valid xml file  
xmllint = find_program('xmllint', required: true)
#if xmllint.found()
#  r = run_command('/usr/bin/xmllint', '--noout', '--xinclude', '--postvalid', 'noent', 'docs/getting-started.xml')
# message (r.returncode()) 
# if r.returncode() != 0
#    error ('Not valid xml file')
#  endif
#endif

if xmllint.found()
  run_target('check-xml',
    command: [
      xmllint,
      '--noout',
      '--xinclude',
      '--postvalid',
      '--noent', 'yocto-main.xml',
    ],
  )
endif

gnome.gtkdoc('yocto-docbook',
	      main_xml : 'yocto-main.xml',
              namespace : 'yocto-docbook',
              src_dir : 'docs',
              html_assets : [
                'images/yocto-logo.png',
              ],
              install: true,
              check: true)
