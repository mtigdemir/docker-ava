# Dockerized AVA Network & Wallet

It was a great experience to be a part of Testnet of Denali. Community is very helpful. 

While, playing with the testnet, hardware and system requirements were pretty strict on builds like Ubuntu 18.94, MacOS Catalina or higher. None of them fit me so docker help as always.


Original AVA network repo has docker container but I was quite interested in running network on my local as well as Wallet. So here we go, simple way to run both and keep yourself upto date on any environment with Docker.


## Installation

1) Clone the repo `` git clone git@github.com:mtigdemir/docker-ava.git ``
2) Go to project `cd docker-ava`
3) Run `docker-compose up`


For more about projects, please visit the below links

[Ava Node (Gecko)](https://github.com/ava-labs/gecko)

[Ava Wallet](https://github.com/ava-labs/ava-wallet)


Give some time to build process then you are good to go, Welcome to Ava Testnet!


Try to create a user

```
curl -X POST --data '{
     "jsonrpc": "2.0",
     "id": 1,
     "method": "keystore.createUser",
     "params": {
         "username": "YOUR USERNAME HERE",
         "password": "YOUR PASSWORD HERE"
     }
}' -H 'content-type:application/json;' 127.0.0.1:9650/ext/keystore
```

If you succeed, visit Wallet `127.0.0.1` and switch to Local AVA Network