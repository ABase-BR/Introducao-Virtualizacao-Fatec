# Vagrantfile e Shell Script

!!! warning "Essa sessão ainda está em desenvolvimento"

     Essa é uma versão básica para servir de referencia para amigos que estão começando.

Podemos criar a maquina rapidamente baixando a VM , e ainda instalar o servidor **NGINX** manualmente e ainda vai ser mais rápido que criar usando a interface do **Virtualbox** mais ainda podemos melhorar.

O **Vagrant** implementa o conceito de provisionamento com drivers para quase todos os sistemas de gerenciamento de configuração existentes. Estes sistemas podem ser simples receitas para instalar pacotes como até agentes que verificam a integridade de arquivos de configuração e variáveis do sistema.

Agora vamos conhecer e utilizar um driver de provisionamento do **Vagrant** que nos permite que um arquivo com comandos do shell sejam executados logo após a criação da sua maquina virtual.

Vamos criar um arquivo chamado **webserver.sh** no mesmo diretório e digite os seguintes comando...

```sh
#!/bin/bash
echo	"Atualizando repositórios"
sudo	 apt-get update
echo	 "Instalando o nginx"
sudo	 apt-get -y install nginx
```

Não esqueça de salvar o arquivo!

Vamos agora editar o arquivo **Vagrantfile** para ativar o provisionador.  Segue o código do arquivo

```sh
#	-*-	mode:	ruby	-*-
#	vi:	set	ft=ruby	:
VAGRANTFILE_API_VERSION	=	"2"
Vagrant.configure(VAGRANTFILE_API_VERSION)	do	|config|
  config.vm.define	"testvm"	do	|testvm|
	 testvm.vm.box	=	"ubuntu/trusty64"
   testvm.vm.network	"public_network", ip: "192.168.0.24"
   testvm.vm.provision	"shell",	path:	"webserver.sh"
  end
	config.vm.provider	"virtualbox"	do	|v|
	 v.customize	["modifyvm",	:id,	"--memory",	"1024"]
	end
end
```

A linha
```sh
 testvm.vm.provision "shell", path: webserver.sh
```

Fica responsavel para dizer para o Vagrant que para aquela VM deve ser usado o **driver** de provisionamento de **shell script** e passa como parâmetro o arquivo com comando que criamos.

Agora podemos **Destruir** e criar a maquina virtual novamente com o **Vagrant**.

Para destruir
```sh
 vagrant destroy
```

Para criar
```sh
 vagrant up
```

Podemos ver que a saída no terminal e faça o mesmo teste que fizemos no navegador sem a necessidade de se conectar por **ssh** para executar os comandos que vai ser responsavel por instalar o **NGINX**.

Agora vamos instalar o PHP5 na VM , vamos modificar o arquivo **webserver.sh**.

```sh
#!/bin/bash
echo	 "Atualizando repositórios"
sudo	 apt-get update
echo	 "Instalando o nginx"
sudo	 apt-get -y install nginx
echo	 "Instalando o PHP"
sudo apt-get install -y php5-fpm

```

Agora não precisamos destruir e recriar a maquina novamente para acontecer o **provisionamento** , contamos com o fato de que o gerenciador de pacotes não instalara um pacote duas vezes.

Poderíamos executar o mesmo script que só o PHP seria instalado.

O **Vagrant** oferece um comando que ativa somente o fase do provisionamento
```sh
 vagrant provision
```

Podemos executar o **vagrant provision** em nosso terminal e observar a execução do script.

Até esse ponto vimos como criar uma descrição de maquina virtual com o **Vagrant** e os seguintes comandos

```sh
vagrant up
vagrant ssh
vagrant destroy
vagrant halt
vagrant provision
```

Com esses comandos conseguimos gerenciar de forma rápida , limpa e segura as maquinas virtuais criadas de acordo com o **Vagrantfile**.

Não se esqueça que eles só funcionaram dentro do diretório em que o **Vagrantfile** estiver.

Podemos executar o comando
```sh
 ls -larth
```

Veja que foi criado um diretório chamado
```sh
 .vagrant
```

Ele contem todos os dados do ciclo de vida e provisionamento da maquina virtual.

## Referências

Caixa de Ferramentas DevOps - ** Gleicon Moraes**
