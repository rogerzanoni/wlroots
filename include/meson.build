subdir('wlr')

exclude_files = ['meson.build', 'config.h.in', 'version.h.in']
if not features.get('x11-backend')
	exclude_files += 'backend/x11.h'
endif
if not features.get('xwayland')
	exclude_files += 'xwayland.h'
else
	subdir('xwayland')
endif

install_subdir('wlr',
	install_dir: get_option('includedir'),
	exclude_files: exclude_files,
)
