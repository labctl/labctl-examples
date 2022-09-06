
### Seamless BFD

# Run the lab

From the current folder, deploy with containerlab

```bash
clab deploy
```

Start the web server by specifying the path to some templates (locally and the shared template folder)

```bash
labctl serve -p ./ -p ../../templates
```

## Info

```
clab deploy
INFO[0000] Containerlab v0.31.1 started
INFO[0000] Parsing & checking topology file: sbfd.clab.yml
INFO[0000] Creating lab directory: /home/kellerza/ip-lab/clab/labctl-examples/random/sros-seamless-bfd/clab-sros-seamless-bfd
INFO[0000] Creating container: "sr2"
INFO[0000] Creating container: "sr1"
INFO[0000] Creating container: "sr3"
INFO[0005] Creating virtual wire: sr2:eth1 <--> sr3:eth2
INFO[0005] Creating virtual wire: sr3:eth1 <--> sr1:eth2
INFO[0005] Creating virtual wire: sr1:eth1 <--> sr2:eth2
INFO[0005] Adding containerlab host entries to /etc/hosts file
+---+----------------------------+--------------+------------------------------------------+---------+---------+-----------------+----------------------+
| # |            Name            | Container ID |                  Image                   |  Kind   |  State  |  IPv4 Address   |     IPv6 Address     |
+---+----------------------------+--------------+------------------------------------------+---------+---------+-----------------+----------------------+
| 1 | clab-sros-seamless-bfd-sr1 | dd261b1923f2 | registry.srlinux.dev/pub/vr-sros:22.7.R1 | vr-sros | running | 172.20.20.15/24 | 2001:172:20:20::f/64 |
| 2 | clab-sros-seamless-bfd-sr2 | 7c2263fd93ae | registry.srlinux.dev/pub/vr-sros:22.7.R1 | vr-sros | running | 172.20.20.13/24 | 2001:172:20:20::d/64 |
| 3 | clab-sros-seamless-bfd-sr3 | 2613b9de2109 | registry.srlinux.dev/pub/vr-sros:22.7.R1 | vr-sros | running | 172.20.20.14/24 | 2001:172:20:20::e/64 |
+---+----------------------------+--------------+------------------------------------------+---------+---------+-----------------+----------------------+
```
