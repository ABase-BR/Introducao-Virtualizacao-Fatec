Todos esses exemplos foram testados nos sistemas operacionais Windows.
- 

## Conhecendo o Power Shell
O powershell é uma ferramenta multiplataforma, está disponivel para
- Windows
- Linux
- Mac

Ela é voltada para automação e configuração de sistema via scripts, ela é bem pareciada com o shell do Linux e Mac.

Para abrir o **powershell** em nossa maquina , podemos executar no **CMD**.
```sh
powershell
```

Com o powershell aberto vamos até o diretorio 
```sh
C:\Program Files\Oracle\VirtualBox
```

Vamos listar o diretorio usando **ls** , ele é chamado de **list** pois ele nos retorna uma listagem de arquivos e diretorios.
```sh
ls
```

## Conhecendo o VBoxManage
O VBoxManage é uma interface de gereciamento via linha de comando , vamos usar ele para controlar nosso virtualbox via linha de comando.
 
Vamos executar o **VBoxManage.exe** , antes vamos checar e ver se estamos no diretorio do virtualbox **C:\Program Files\Oracle\VirtualBox**.

Podemos usar o **pwd** para ver em qual diretorio estamos.
```sh
pwd
```

Vamos executar ele da seguinte forma , sem passar argumento para usar o padrão;
```sh
./VBoxManage.exe 
```

Podemos verificar a versão atual usando
```sh
./VBoxManage.exe -v
```

## Listando maquinas virtuais
Podemos listar maquinas usando o **list vms**.

Veja um exemplo a baixo seguido da imagem.
```sh
./VBoxManage.exe list vms
```


Podemos ver o retorno na nossa maquina

![Listar VMS](https://raw.githubusercontent.com/ABase-BR/abase-br.github.io/master/images/Virtualbox/CLI/Virtualbox-CLI-listar-VMS.png)

Podemos ver a saida da minha maquina , a sua vai ser diferente dependendo do numero de maquinas que estiver usando.
```sh
"Android" {d801c129-a7b4-401b-982d-df53a67cc1d3}
"FreeBSD_11.1_amd64" {e01d7ecb-bde3-4fd2-8fa1-2991e47ad9c4}
"Debian_stretch_X64" {b6b276ab-999b-4782-9f53-04f3a7e5f002}
"Windows 7" {c8e67740-8441-46d5-9f00-7e51c36bc4bc}
"Clone_Windows_7_Home_Premium" {1a4e6407-c20b-4dfc-a8a8-b8d8a86f192b}
"Clone_Android" {7088de9c-bc14-493b-a5eb-eb1b63bc2c8a}
"DebianServer" {d166c1a8-8e56-4724-b04a-8f5ce84bffeb}
"Clone de DebianServer" {1f3cd8e8-a6b0-4845-b5b5-113ae9018388}
"ABase" {e32647f6-70e0-44aa-9374-feae2ef30be3}
"WindowsXP" {62135601-fa65-4007-bad2-965a4ae5ce6f}
"pentest-env-kali-rolling" {7145c301-6cea-4456-bf0b-7f9e30f8322b}
"Clone de WindowsXP" {304bb845-3e05-4272-8c3d-2556d8563f32}
```

## Iniciando maquina virtual
Para iniciar uma VM só precisamos usar o **startvm** seguido do nome da VM.

Vamos iniciar o DebianServer
```sh
./VBoxManage.exe startvm DebianServer 
```

## Importando uma VM
Podemos importar uma maquina via linha de comando da seguinte forma , vamos imaginar que nossa imagem baixada está na area de trabalho.

A maquina usada é a
- kali-linux-2018.3-vm-amd64.ova

O local onde ele está é
```sh
C:\Users\Administrador\Desktop\
```

O comando completo fica
```sh
.\VBoxManage.exe import 'C:\Users\Administrador\Desktop\kali-linux-2018.3-vm-amd64.ova'
```

Depois de dar o comando podemos ver que ele vai ser retornado informações da VM

![Instalando Extension Pack](https://github.com/ABase-BR/abase-br.github.io/blob/master/images/Virtualbox/CLI/Virtualbox-CLI-1.png)

Podemos ver o comando inteiro na imagem a baixo

![Instalando Extension Pack](https://github.com/ABase-BR/abase-br.github.io/blob/master/images/Virtualbox/CLI/Virtualbox-CLI-2.png)

E se tudo der certo vamos ver a mensagem de retorno.

![Instalando Extension Pack](https://github.com/ABase-BR/abase-br.github.io/blob/master/images/Virtualbox/CLI/Virtualbox-CLI-3.png)