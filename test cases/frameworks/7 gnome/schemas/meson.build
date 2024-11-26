
compiled = gnome.compile_schemas(build_by_default: true)
install_data('com.github.meson.gschema.xml',
install_dir : 'share/glib-2.0/schemas')

testenv = environment()
testenv.append('GSETTINGS_SCHEMA_DIR', meson.current_build_dir())

schemaexe = executable('schemaprog', 'schemaprog.c', dependencies : gio, install: true)
test('schema test', schemaexe, env: testenv)
