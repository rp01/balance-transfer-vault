# balance-transfer-vault
fork of https://github.com/hyperledger/fabric-samples/tree/release-1.4/balance-transfer with implimentation of hashicorp' vault

if you are getting error as 
Some Times you may get error ```Error: Status 404``` even in setting values. just open another terminal tab/window run:

```
export VAULT_TOKEN=<TOKEN> 
export VAULT_ADDRESS='http(s)://<HOST>:<PORT>'
````

Then run the following command:

```
vault secrets disable secret
vault secrets enable -version=1 -path=secret kv
```

This example requuires to vault instanses. Assuming vault is already installed

to run multiple instanses
run :
```
vault server -dev
```
and in a separate tab 
```
vault server -dev -dev-listen-address=127.0.0.1:8300
```