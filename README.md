# certctl


# TODO: support subcommands

If you use default output names, then subsequent commands require fewer flags.

Create CA:

```
certctl ca init --name <name>
certctl ca status
```

Create issuer certificate for servers:

```
certctl issuer --server --name <thing>
```

Issue a server certificate:

```
certctl server --hostname <thing> --alt 192.168.1.1
```

