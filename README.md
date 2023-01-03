# Tutorial linux redes

## Links

### Calculadora de IPs
https://jodies.de/ipcalc?host=10.10.3.6&mask1=28&mask2=

### AWS latency test
https://aws-latency-test.com


## Arquivos

### Configuraçao dos servidores de DNS utilizados
- Para configurar, pode-se editar o arquivo. <br>
  No Windows, executar ```ipconfig /all```.
```sh
cat /etc/resolv.conf
```

### Para forçar um IP sem usar o DNS (pode ser usado para testes)
- Adicionar uma nova linha no arquivo /etc/hosts.
```sh
cat /etc/hosts
```

### Para saber as portas usadas por cada serviço
- Verificar arquivo /etc/services.
```sh
cat /etc/services
```


## Comandos

### curl
- Conecta e traz o conteudo de um site.
```sh
curl https://www.google.com
```

- Conecta e traz o cabeçalho (header) do site, bem como o codigo HTTP do retorno da requisiçao.
```sh
curl -I https://www.google.com
```

- Para saber op IP publico da maquina
```sh
curl ifconfig.me
```

### dig
- Além de resolver um nome, diz o endereço IP do servidor de DNS (ver campo SERVER).
```sh
dig google.com
```

- Resolvendo um nome, dizendo o IP de um servidor de DNS especifico (8.8.8.8 - DNS do Google).
```sh
dig @8.8.8.8 google.com
```

- Resolver um nome em endereço IP v6.
```sh
dig www.google.com AAAA
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

### ping
- Verifica se via protocolo ICMP se consegue chegar a um determinado endereço. <br>
  Também, se obtém o IP resolvido e o tempo para um pacote ir para e voltar deste endereço.
```sh
ping www.google.com
```

### tcpdump
- Para capturar pacotes na maquina. <br>
  Pode-se filtrar os pacotes por protocolo, host e porta. <br>
  Detalhes em: https://opensource.com/article/18/10/introduction-tcpdump
```sh
sudo tcpdump port 80 -v -n
```

### telnet
- Pode-se usar o telnet para verificar se uma porta esta aberta. <br>
  Para sair do telnet no MacOS, teclado frances canadense : CTRL + Ç. <br>
  Na maioria dos teclados: CTRL + ]. <br>
  Apos, usar: quit.
```sh
telnet www.gov.br 80
```

### traceroute
- Verificando a rota até o DNS do Google. <br>
  No Windows: ```tracert```.
```sh
traceroute 8.8.8.8
```

- Verificando a rota até o DNS do Google, usando o protocolo ICMP.
```sh
traceroute -I 8.8.8.8
```

