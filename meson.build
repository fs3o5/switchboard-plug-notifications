project(
    'notifications',
    'vala', 'c',
    version: '2.1.7'
)

gettext_name = meson.project_name() + '-plug'
gnome = import('gnome')
i18n = import('i18n')

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
libdir = join_paths(prefix, get_option('libdir'))

add_project_arguments(
    '-DGETTEXT_PACKAGE="@0@"'.format(gettext_name),
    language:'c'
)

plug_resources = gnome.compile_resources(
    'plug_resources',
    'data/switchboard-plug-notifications.gresource.xml',
    source_dir: 'data'
)

subdir('data')
subdir('src')
subdir('po')
