<!-- markdownlint-disable -->
## talosctl copy

Copy data out from the node

### Synopsis

Creates an .tar.gz archive at the node starting at <src-path> and
streams it back to the client.

If '-' is given for <local-path>, archive is written to stdout.
Otherwise archive is extracted to <local-path> which should be an empty directory or
talosctl creates a directory if <local-path> doesn't exist. Command doesn't preserve
ownership and access mode for the files in extract mode, while  streamed .tar archive
captures ownership and permission bits.

```
talosctl copy <src-path> -|<local-path> [flags]
```

### Options

```
  -h, --help   help for copy
```

### Options inherited from parent commands

```
      --context string       Context to be used in command
  -e, --endpoints strings    override default endpoints in Talos configuration
  -n, --nodes strings        target the specified nodes
      --talosconfig string   The path to the Talos configuration file (default "/home/user/.talos/config")
```

### SEE ALSO

* [talosctl](talosctl.md)	 - A CLI for out-of-band management of Kubernetes nodes created by Talos

