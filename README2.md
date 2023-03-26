Assignment1
Part 2

docker run:Runs an image
viru@viru:~$ sudo docker run assign1p1
Hello, This is my first image file.

docker ps:Shows running containers
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

docker ps -a:Show all containers
viru@viru:~$ sudo docker ps -a
CONTAINER ID   IMAGE       COMMAND                  CREATED              STATUS                          PORTS     NAMES
b9df1c994323   assign1p1   "echo 'Hello, This i…"   About a minute ago   Exited (0) About a minute ago             romantic_wilson
0b15be806e81   ubuntu      "/bin/bash"              38 hours ago         Exited (0) 38 hours ago                   gracious_jepsen
e0d875508823   assign1p1   "echo 'Hello, This i…"   38 hours ago         Exited (0) 38 hours ago                   stupefied_proskuriakova
7183b5e5d0de   assign1p1   "echo 'Hello, This i…"   2 days ago           Exited (0) 2 days ago                     flamboyant_rubin

docker stop:Stops a container
viru@viru:~$ sudo docker stop stupefied_proskuriakova
stupefied_proskuriakova

docker rm:Remove a container
viru@viru:~$ sudo docker rm stupefied_proskuriakova
stupefied_proskuriakova
viru@viru:~$ sudo docker ps -a
CONTAINER ID   IMAGE       COMMAND                  CREATED         STATUS                     PORTS     NAMES
b9df1c994323   assign1p1   "echo 'Hello, This i…"   5 minutes ago   Exited (0) 5 minutes ago             romantic_wilson
0b15be806e81   ubuntu      "/bin/bash"              38 hours ago    Exited (0) 38 hours ago              gracious_jepsen
7183b5e5d0de   assign1p1   "echo 'Hello, This i…"   2 days ago      Exited (0) 2 days ago                flamboyant_rubin

docker logs:Shows command logs of a container
viru@viru:~$ sudo docker logs b9df1c994323
Hello, This is my first image file.

docker inspect:Shows detail logs of a container
viru@viru:~$ sudo docker inspect romantic_wilson
[
    {
        "Id": "b9df1c994323370ab90cddb1ea190362b8ff11de3cf106c40b7c60eed4485016",
        "Created": "2023-03-26T07:18:07.276547141Z",
        "Path": "echo",
        "Args": [
            "Hello, This is my first image file."
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-03-26T07:18:10.068625789Z",
            "FinishedAt": "2023-03-26T07:18:10.228455869Z"
        },
        "Image": "sha256:76836b45f39f429d6be4d82d24d246005ebe7b6c62af7a711b2ac6a3c8faf30f",
        "ResolvConfPath": "/var/lib/docker/containers/b9df1c994323370ab90cddb1ea190362b8ff11de3cf106c40b7c60eed4485016/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/b9df1c994323370ab90cddb1ea190362b8ff11de3cf106c40b7c60eed4485016/hostname",
        "HostsPath": "/var/lib/docker/containers/b9df1c994323370ab90cddb1ea190362b8ff11de3cf106c40b7c60eed4485016/hosts",
        "LogPath": "/var/lib/docker/containers/b9df1c994323370ab90cddb1ea190362b8ff11de3cf106c40b7c60eed4485016/b9df1c994323370ab90cddb1ea190362b8ff11de3cf106c40b7c60eed4485016-json.log",
        "Name": "/romantic_wilson",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                30,
                120
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/5ded7d56920a30855c453829e255b98914f3ccf6c9f3be2844edb33b014fe6f9-init/diff:/var/lib/docker/overlay2/855330nosppeuhe5jtvgrkfyi/diff:/var/lib/docker/overlay2/f398f77f9a2f38a22f4fb9f892893faae7fe1f37356a7290383846bfd536557a/diff",
                "MergedDir": "/var/lib/docker/overlay2/5ded7d56920a30855c453829e255b98914f3ccf6c9f3be2844edb33b014fe6f9/merged",
                "UpperDir": "/var/lib/docker/overlay2/5ded7d56920a30855c453829e255b98914f3ccf6c9f3be2844edb33b014fe6f9/diff",
                "WorkDir": "/var/lib/docker/overlay2/5ded7d56920a30855c453829e255b98914f3ccf6c9f3be2844edb33b014fe6f9/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "b9df1c994323",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": true,
            "AttachStderr": true,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "echo",
                "Hello, This is my first image file."
            ],
            "Image": "assign1p1",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "org.opencontainers.image.ref.name": "ubuntu",
                "org.opencontainers.image.version": "22.04"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "3c9cef63ff8f98d32bc2d7ffb33bdfc672401bf0fdf092ee634a890f4ec7636f",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {},
            "SandboxKey": "/var/run/docker/netns/3c9cef63ff8f",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "a880f41d293146c57be632ca6f4fbd000d5aa6463552f7868f9f7c3a43354cf5",
                    "EndpointID": "",
                    "Gateway": "",
                    "IPAddress": "",
                    "IPPrefixLen": 0,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "",
                    "DriverOpts": null
                }
            }
        }
    }
]


docker exec:Executes command on a running container
viru@viru:~$ sudo docker run -d ubuntu sleep infinity
a98b2c6df0e66e02f0dc590ee58cc62920a70a8dc870479340f84212eaf45868
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND            CREATED         STATUS         PORTS     NAMES
a98b2c6df0e6   ubuntu    "sleep infinity"   7 seconds ago   Up 4 seconds             thirsty_austin
viru@viru:~$ sudo docker exec thirsty_austin echo "Hello world"
Hello world

docker attach:Attach a command to a running container
viru@viru:~$ sudo docker attach romantic_wilson
You cannot attach to a stopped container, start it first

docker commit:Add a tag to a container
viru@viru:~$ sudo docker commit b9df1c994323 jack/first:ver4
sha256:27979eeb31dc612694fd25d1e9e0f7ea487cf46b9d26a22a3d3e802ad8f68bc3
viru@viru:~$ sudo docker images
REPOSITORY           TAG          IMAGE ID       CREATED          SIZE
jack/first           ver4         27979eeb31dc   11 seconds ago   77.8MB
hamiz822/dockerhub   firstimage   76836b45f39f   2 days ago       77.8MB
assign1p1            latest       76836b45f39f   2 days ago       77.8MB
ubuntu               latest       08d22c0ceb15   2 weeks ago      77.8MB

docker stats:Shows live status of containers
viru@viru:~$ sudo docker stats
CONTAINER ID   NAME      CPU %     MEM USAGE / LIMIT   MEM %     NET I/O   BLOCK I/O   PIDS
^C
viru@viru:~$ sudo docker stats --help
Usage:  docker stats [OPTIONS] [CONTAINER...]
Display a live stream of container(s) resource usage statistics
Aliases:
  docker container stats, docker stats
Options:
  -a, --all             Show all containers (default shows just running)
      --format string   Format output using a custom template:
                        'table':            Print output in table format with column headers (default)
                        'table TEMPLATE':   Print output in table format using the given Go template
                        'json':             Print in JSON format
                        'TEMPLATE':         Print output using the given Go template.
                        Refer to https://docs.docker.com/go/formatting/ for more information about formatting
                        output with templates
      --no-stream       Disable streaming stats and only pull the first result
      --no-trunc        Do not truncate output

docker top:Display the running processes of a container
viru@viru:~$ sudo docker top 4c4ac499d371
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                4491                4469                0                   13:24               ?                   00:00:00            sleep infinity

docker start:Starts a container
viru@viru:~$ sudo docker start b9df1c994323
b9df1c994323

docker pause:Pause a container
viru@viru:~$ sudo docker pause 4c4ac499
4c4ac499
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND            CREATED         STATUS                  PORTS     NAMES
4c4ac499d371   ubuntu    "sleep infinity"   5 minutes ago   Up 5 minutes (Paused)             flamboyant_austin

docker unpause:Unpause a container
viru@viru:~$ sudo docker unpause 4c4ac499
4c4ac499
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND            CREATED         STATUS         PORTS     NAMES
4c4ac499d371   ubuntu    "sleep infinity"   5 minutes ago   Up 5 minutes             flamboyant_austin

docker rename:Rename a container
viru@viru:~$ sudo docker rename 4c4ac INFI
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND            CREATED         STATUS         PORTS     NAMES
4c4ac499d371   ubuntu    "sleep infinity"   8 minutes ago   Up 8 minutes             INFI


docker wait:Block until one or more containers stop, then print their exit codes
viru@viru:~$ sudo docker wait
"docker wait" requires at least 1 argument.
See 'docker wait --help'.
Usage:  docker wait CONTAINER [CONTAINER...]

docker port:Shows avaliable ports of the container
viru@viru:~$ sudo docker port 4c4ac499d371 25
Error: No public port '25' published for 4c4ac499d371

docker restart:Update configuration of one or more containers
viru@viru:~$ sudo docker update --help
Usage:  docker update [OPTIONS] CONTAINER [CONTAINER...]
Aliases:
  docker container update, docker update
Options:
      --blkio-weight uint16        Block IO (relative weight), between 10 and 1000, or 0 to disable (default 0)
      --cpu-period int             Limit CPU CFS (Completely Fair Scheduler) period
      --cpu-quota int              Limit CPU CFS (Completely Fair Scheduler) quota
      --cpu-rt-period int          Limit the CPU real-time period in microseconds
      --cpu-rt-runtime int         Limit the CPU real-time runtime in microseconds
  -c, --cpu-shares int             CPU shares (relative weight)
      --cpus decimal               Number of CPUs
      --cpuset-cpus string         CPUs in which to allow execution (0-3, 0,1)
      --cpuset-mems string         MEMs in which to allow execution (0-3, 0,1)
  -m, --memory bytes               Memory limit
      --memory-reservation bytes   Memory soft limit
      --memory-swap bytes          Swap limit equal to memory plus swap: -1 to enable unlimited swap
      --pids-limit int             Tune container pids limit (set -1 for unlimited)
      --restart string             Restart policy to apply when a container exits

docker restart:Restart one or more containers
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND            CREATED          STATUS          PORTS     NAMES
4c4ac499d371   ubuntu    "sleep infinity"   13 minutes ago   Up 13 minutes             INFI
viru@viru:~$ sudo docker restart 4c4ac
4c4ac
viru@viru:~$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND            CREATED          STATUS         PORTS     NAMES
4c4ac499d371   ubuntu    "sleep infinity"   14 minutes ago   Up 6 seconds             INFI

