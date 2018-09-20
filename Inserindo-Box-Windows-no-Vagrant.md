# Baixando maquina Windows XP SP3
!!! warning "Essa sessão ainda está em desenvolvimento"

     Essa é uma versão básica para servir de referencia para amigos que estão começando.

Vamos iniciar criando um diretório para nossa maquina virtual
```sh
 mkdir WindowsXP_SP3
```

Em seguida vamos entrar em nosso diretório
```sh
  cd WindowsXP_SP3
```

Ainda em nosso terminal vamos inserir o seguinte comando para baixar a Box que está nesse link
```sh
 https://atlas.hashicorp.com/billryan/boxes/win-xp-sp3
```

**Caso esteja usando Virtualbox** faça o seguinte comando
```sh
 vagrant init billryan/win-xp-sp3; vagrant up --provider virtualbox
```

Caso não de certo , execute o comando com permissão de administrador (recomendo o uso do SUDO para maior segurança)

## Baixando maquina Windows 7 SP1
Vamos iniciar criando um diretório para nossa maquina virtual
```sh
 mkdir Windows7_SP1
```

Em seguida vamos entrar em nosso diretório
```sh
  cd Windows7_SP1
```

Ainda em nosso terminal vamos inserir o seguinte comando para baixar a Box que está nesse link
```sh
 https://atlas.hashicorp.com/ramreddy06/boxes/windows7-sp1
```

**Caso esteja usando Virtualbox** faça o seguinte comando
```sh
 vagrant init ramreddy06/windows7-sp1; vagrant up --provider virtualbox
```

Caso não de certo , execute o comando com permissão de administrador (recomendo o uso do SUDO para maior segurança)
