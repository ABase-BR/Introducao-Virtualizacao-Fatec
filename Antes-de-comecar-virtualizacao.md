# Antes de começar - Virtualização

Antes de montar um ambiente de produção ou desenvolvimento é necessário ter uma maquina , seja ela um computador , notebook ou até um servidor dedicado.

Com vimos anteriormente em **O que é Virtualização** podemos criar maquinas virtuais em nossa maquina **host** e assim reduzindo o desperdicio de recursos.

Podemos executar diversas maquinas em uma unica maquina física funcionando juntas. 

Podemos utilizar projetos como **XenProject** , **Virtualbox** , **Parallels** e até **VmWare** para gerenciar e executar as maquinas.

Uma maquina virtual nada mais é que uma imagem de disco e metadados que descrevem a sua configuração e estado:

- Processador 
- Memoria 
- Discos 
- Conexões externas

Lembre-se que a maquina em execução é um processo que vai depender de um **Agendados de tarefas e processos** ou **scheduler** que é responsável por coordenar o uso dos recursos locais.

Podemos gerenciar nossas maquinas virtuais diretamente das interfaces dos projetos 

- XenProject
- Virtualbox
- Parallels
- VmWare
 
Tambem podemos utilizar bibliotecas ou até sistemas que desconsidera as diferenças entre as plataformas , com a interface podemos 

- Criar 
- Executar 
- Parar 
- Modificar uma maquina virtual

Não podemos esquecer que é importante na escolha do sistema levar em consideração que existe diversos formatos de maquinas virtuais , diferentes sistemas operacionais e precisamos ficar de olho no formato de templates.

É importante que tenhamos também fontes para maquinas virtuais , futuramente veremos fontes oficiais de imagens , de inicio vamos começar criando maquinas virtuais com um sistema operacional original e também vamos criar nossas maquinas.

Depois da criação da maquina virtual podemos executar um passo posterior que chamamos de **provisionameto** para modificar o sistema operacional. 

Podemos instalar pacotes e realizar configurações , alem de instalar nossa aplicação e até salvar aquela versão da maquina virtual para uso posterior.

## Referências

Caixa de Ferramentas DevOps - **Gleicon Moraes**

