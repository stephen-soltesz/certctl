# certctl


# TODO: support subcommands

If you use default output names, then subsequent commands require fewer flags.

Create CA:

```
certctl ca init --name <name>
certctl ca info
```

Create intermediate issuing certificate signed by the CA:

```
certctl intermediate init --server --name <thing>
certctl intermediate info
```

Create server certificate signed by issuing certificate:

```
certctl server init --hostname <thing> --alt 192.168.1.1
certctl server info
```

## Examples with OpenSSL

Create CSR:

```
openssl genrsa -out domain.com.key 2048
openssl req -new -sha256 -key domain.com.key -out domain.com.csr
openssl req -noout -text -in domain.com.csr
```
