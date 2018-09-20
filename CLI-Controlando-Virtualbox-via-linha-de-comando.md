## Listando maquinas virtuais

VBoxManage list vms

Podemos ver a saida da minha maquina
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

VBoxManage startvm


Vamos iniciar o DebianServer
```sh
VBoxManage startvm DebianServer 
```


## Controlando VM
Vamos ver a rede do servidor debian.

