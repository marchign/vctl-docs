## vctl system prepare

Prepare host OS for Nautilus Container Engine.

### Synopsis

Prepare storage and network for Nautilus Container Engine.

```
vctl system prepare [options]
```

### Options

```
  -c, --cache-location string   Specify a location to store cache file (default "/Users/xiaodongy/.nautilus")
  -s, --dmg-size string         dmg file size (default "128g")
  -h, --help                    help for prepare
  -m, --mount-name string       Mount name for container storage (default "nautilus")
  -u, --vm-cpu int              CPU cores of base virtual machine (default 2)
  -o, --vm-mem int              Memory size (MB) of base virtual machine (default 1024)
```

### SEE ALSO

* [vctl system](vctl_system.md)	 - Manage Nautilus Container Engine.

###### Auto generated by spf13/cobra on 16-Jan-2020