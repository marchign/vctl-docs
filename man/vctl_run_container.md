## vctl run container

Run a new container from an image.

### Synopsis

Create and start a container with the given name, from the specified image, then run a command in it.
* If no COMMAND is provided, the default command from the image will be executed.
* If the COMMAND to execute has any flags in common [e.g. -t], two dashes '--' must be used to separate the COMMAND's flags/arguments.

```
vctl run container CONTAINER_NAME --image=IMAGE [options] -- [COMMAND] [arguments...]
```

### Examples

```
  # To run 'date' in a new container with the name of 'myContainer' using 'myImage' image.
  vctl run container myContainer --image=myImage date
  # To list contents of myContainer and sort by the modification time. ['--' must be used here to seperate '-t'].
  vctl run container myContainer --image=myImage -- ls -t
  # To run myContainer using default command and set environment variables "FOO=BAR" in myContainer.
  vctl run container myContainer --image=myImage --env="FOO=BAR"
```

### Options

```
      --cwd string        Working directory of the new process
  -d, --detach            Detach from the task once the execution starts
  -e, --env strings       Environment variables to set in the container
  -h, --help              help for container
      --hostname string   Host name of the container
  -i, --image string      The image required for the container to run
  -k, --keepVM-exp        [EXPERIMENTAL] Keep host virtual machine running after container stops
  -p, --publish strings   Bind host network ports to container ports
  -t, --tty               Allocate a TTY for the container
  -v, --volume strings    Bind host folders to container folders
```

### SEE ALSO

* [vctl run](vctl_run.md)	 - Run containers from images.

###### Auto generated by spf13/cobra on 16-Jan-2020