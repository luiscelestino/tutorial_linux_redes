# Tutorial linux redes

## ip addr
- Novo comando que verifica detalhes de IP e endereço de broadcast (normalmente, o ultimo endereço na rede). <br>
  Interfaces padroes: eth0, en0. <br>
  No MacOS, é necessario instalar o iproute2mac (brew install iproute2mac).
```sh
ip addr
```

## ip route
- Comando para ver qual é o endereço do roteador (gateway). <br>
  O roteador é incado pelo valor default. <br>
  No MacOS, é necessario instalar o iproute2mac (brew install iproute2mac).
```sh
ip route
```


## nslookup
- Verifica o endereço IP de um nome na internet
```sh
nslookup google.com
```

