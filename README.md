# certctl


# TODO: support subcommands

If you use default output names, then subsequent commands require fewer flags.

Create CA:

```
certctl create ca --name <name>
certctl status ca
```

Create intermediate issuing certificate signed by the CA:

```
certctl create intermediate --server --name <thing>
certctl status intermediate
```

Create server certificate signed by issuing certificate:

```
certctl create server --hostname <thing> --alt 192.168.1.1
certctl status server
```

## Examples with OpenSSL

Create CSR:

```
openssl genrsa -out domain.com.key 2048
openssl req -new -sha256 -key domain.com.key -out domain.com.csr
openssl req -noout -text -in domain.com.csr
```
