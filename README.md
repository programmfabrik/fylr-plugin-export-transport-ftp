# fylr-plugin-export-transport-ftp

The **fylr** plugin for FTP and WebDAV export transports: exports are handed
to a python callback that uploads the export files via rclone.

Split from
[easydb-export-transport-ftp-plugin](https://github.com/programmfabrik/easydb-export-transport-ftp-plugin),
which continues to serve easydb 5 unchanged — this repo is fylr-only and is
built by [fylr-build-plugin](https://github.com/programmfabrik/fylr-build-plugin);
see there for how a fylr plugin is structured. Run `make` for the target list.
The plugin name `easydb-export-transport-ftp-plugin` is kept from the ez5 era
so saved export transport configurations keep working.

fylr installs the plugin from the latest release:

```
https://github.com/programmfabrik/fylr-plugin-export-transport-ftp/releases/latest/download/fylr-plugin-export-transport-ftp.zip
```

The loca CSV is mastered in the shared Google Sheet — edit there and run
`make loca`, never edit the CSV directly. `server/fylr_lib_plugin_python3` is
a git submodule; clone with `--recursive`.
