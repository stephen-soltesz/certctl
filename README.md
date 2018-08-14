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

## Examples with OpenSSL

Create CSR:

```
openssl genrsa -out domain.com.key 2048
openssl req -new -sha256 -key domain.com.key -out domain.com.csr
openssl req -noout -text -in domain.com.csr
```
