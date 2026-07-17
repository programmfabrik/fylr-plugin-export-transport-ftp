# fylr-plugin-export-transport-ftp

A [fylr](https://docs.fylr.io) plugin adding two **export transports**:
**FTP** and **WebDAV**. When an export finishes, the plugin uploads the export
files to the configured target server using [rclone](https://rclone.org)
(which must be available on the server running the callbacks).

In the export manager, each export can be given one or more transports; this
plugin contributes the FTP and WebDAV transport types with their connection
settings (server, credentials, target directory, …). The upload runs
server-side with a generous timeout (1 hour) for large exports.

## Installation

Open the fylr Plugin Manager and add a new plugin of type "url". This URL
always links to the latest released version:

```
https://github.com/programmfabrik/fylr-plugin-export-transport-ftp/releases/latest/download/fylr-plugin-export-transport-ftp.zip
```

## Configuration

Transports are configured per export in the export manager. In the base
configuration (system settings → Export), *rclone debug logging* can be
enabled to diagnose transport problems — rclone's output then appears in the
server log.

## Building

Built by [fylr-build-plugin](https://github.com/programmfabrik/fylr-build-plugin);
run `make` for the target list (`make build` assembles
`build/easydb-export-transport-ftp-plugin/`, loadable by fylr from disk for
development). `server/fylr_lib_plugin_python3` is a git submodule — clone with
`--recursive`. The loca CSV is mastered in a Google Sheet — edit there and run
`make loca`, never edit the CSV directly.

## Contact

For issues and questions please use
[the issue tracker](https://github.com/programmfabrik/fylr-plugin-export-transport-ftp/issues)
or write to support@programmfabrik.de.

---

*This plugin was forked for fylr from
[easydb-export-transport-ftp-plugin](https://github.com/programmfabrik/easydb-export-transport-ftp-plugin),
which continues to serve easydb 5 unchanged. The plugin name
`easydb-export-transport-ftp-plugin` is deliberately kept, so saved export
transport configurations keep working.*
