<!-- markdownlint-disable -->
## talosctl cluster create

Creates a local docker-based or firecracker-based kubernetes cluster

### Synopsis

Creates a local docker-based or firecracker-based kubernetes cluster

```
talosctl cluster create [flags]
```

### Options

```
      --cidr string                 CIDR of the docker bridge network (default "10.5.0.0/24")
      --cni-bin-path strings        search path for CNI binaries (default [/opt/cni/bin])
      --cni-cache-dir string        CNI cache directory path (default "/var/lib/cni")
      --cni-conf-dir string         CNI config directory path (default "/etc/cni/conf.d")
      --cpus string                 the share of CPUs as fraction (each container) (default "1.5")
      --disk int                    the limit on disk size in MB (each VM) (default 4096)
      --endpoint string             use endpoint instead of provider defaults
  -p, --exposed-ports string        Comma-separated list of ports/protocols to expose on init node. Ex -p <hostPort>:<containerPort>/<protocol (tcp or udp)> (Docker provisioner only)
  -h, --help                        help for create
      --image string                the image to use (default "docker.io/autonomy/talos:latest")
      --init-node-as-endpoint       use init node as endpoint instead of any load balancer endpoint
      --initrd-path string          the uncompressed kernel image to use (default "_out/initramfs.xz")
  -i, --input-dir string            location of pre-generated config files
      --install-image string        the installer image to use (default "docker.io/autonomy/installer:latest")
      --kubernetes-version string   desired kubernetes version to run (default "1.18.0")
      --masters int                 the number of masters to create (default 1)
      --memory int                  the limit on memory usage in MB (each container) (default 1024)
      --mtu int                     MTU of the docker bridge network (default 1500)
      --nameservers strings         list of nameservers to use (VM only) (default [8.8.8.8,1.1.1.1])
      --registry-mirror strings     list of registry mirrors to use in format: <registry host>=<mirror URL>
      --vmlinux-path string         the uncompressed kernel image to use (default "_out/vmlinux")
      --wait                        wait for the cluster to be ready before returning (default true)
      --wait-timeout duration       timeout to wait for the cluster to be ready (default 20m0s)
      --with-bootloader-emulation   enable bootloader emulation to load kernel and initramfs from disk image
      --with-debug                  enable debug in Talos config to send service logs to the console
      --with-init-node              create the cluster with an init node (default true)
      --workers int                 the number of workers to create (default 1)
```

### Options inherited from parent commands

```
      --context string       Context to be used in command
  -e, --endpoints strings    override default endpoints in Talos configuration
      --name string          the name of the cluster (default "talos-default")
  -n, --nodes strings        target the specified nodes
      --provisioner string   Talos cluster provisioner to use (default "docker")
      --state string         directory path to store cluster state (default "/home/user/.talos/clusters")
      --talosconfig string   The path to the Talos configuration file (default "/home/user/.talos/config")
```

### SEE ALSO

* [talosctl cluster](talosctl_cluster.md)	 - A collection of commands for managing local docker-based or firecracker-based clusters

