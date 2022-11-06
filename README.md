# docker-vagrant
Laboratório de criação de máquina virtuais com vagrant, com docker já instalado


Dependências
-------------

Para a criação do laboratório é necessário ter pré instalado os seguintes softwares:

* [Git][1]
* [VirtualBox][2]
* [Vagrant][3]

> Para as máquinas com Windows, é aconselhado que as instalações, provisionamento e execução de comandos sejam feitos pelo  **[Cygwin][5]**. Caso você opte por outro cmd ou gerenciador git, como o **[gitforwindows][10]**, antes de iniciar o provisionamento, execute o comando `git config --global core.autocrlf false` para evitar quebras de linhas.

> Para as máquinas com Windows, é necessário que o [Hyper-V][9] esteja `desabilitado`.

Laboratório
-----------

O Laboratório será criado utilizando o [Vagrant][6]. Ferramenta para criar e gerenciar ambientes virtualizados (baseado em Inúmeros providers) com foco em automação.

Nesse laboratório, que está centralizado no arquivo [Vagrantfile][7], sera criada 1 maquina com a seguinte característica:

Nome       | vCPUs | Memoria RAM | IP            | S.O.¹           
---------- |:-----:|:-----------:|:-------------:|:---------------:
master     | 1     | 1024MB | 192.168.99.100 | ubuntu/bionic64
node1      | 1     | 1024MB | 192.168.99.101 | ubuntu/bionic64
node2      | 1     | 1024MB | 192.168.99.102 | ubuntu/bionic64
node3      | 1     | 1024MB | 192.168.99.103 | ubuntu/bionic64

>  Esses Sistemas operacionais estão sendo utilizado no formato de Boxes, é a forma como o vagrant chama as imagens do sistema operacional utilizado.
>  A memória inicial de cada VM está definida com 1024MB (1GB). Este valor pode ser aumentado, caso necessário através do arquivo `Vagrantfile`.

Criação do Laboratório
----------------------

Para criar o laboratório é necessário fazer o `git clone` desse repositório e, dentro da pasta baixada realizar a execução do `vagrant up`, conforme abaixo:

```bash
git clone https://github.com/4linux/4528
cd 4528/
vagrant up
```





[1]: https://git-scm.com/downloads
[2]: https://www.virtualbox.org/wiki/Downloads
[3]: https://www.vagrantup.com/downloads
[5]: https://cygwin.com/install.html
[6]: https://www.vagrantup.com/
[7]: ./Vagrantfile
[8]: https://www.vagrantup.com/docs
[9]: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/
[10]: https://gitforwindows.org/
