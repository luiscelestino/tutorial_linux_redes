# Tutorial linux redes

## Links

### Calculadora de IPs
https://jodies.de/ipcalc?host=10.10.3.6&mask1=28&mask2=

## Arquivos

### Configuraçao dos servidores de DNS utilizados
```sh
cat /etc/resolv.conf
```

## Comandos

### dig
- Além de resolver um nome, diz o endereço IP do servidor de DNS (ver campo SERVER).
```sh
dig google.com
```

- Resolvendo um nome, dizendo o IP de um servidor de DNS especifico (8.8.8.8 - DNS do Google).
```sh
dig @8.8.8.8 google.com
```

### ifconfig
- Antigo comando que verifica detalhes de IP e endereço de broadcast (normalmente, o ultimo endereço na rede). <br>
  Interfaces padroes: eth0, en0.
```sh
ip addr
```

### ip addr
- Novo comando que verifica detalhes de IP e endereço de broadcast (normalmente, o ultimo endereço na rede). <br>
  Interfaces padroes: eth0, en0. <br>
  No MacOS, é necessario instalar o iproute2mac (brew install iproute2mac).
```sh
ip addr
```

### ip route
- Comando para ver qual é o endereço do roteador (gateway). <br>
  O roteador é incado pelo valor default. <br>
  No MacOS, é necessario instalar o iproute2mac (brew install iproute2mac).
```sh
ip route
```

### nslookup
- Verifica o endereço IP de um nome na internet
```sh
nslookup google.com
```
