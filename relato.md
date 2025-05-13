# Relato - Atividade 02 - utilizando linux no windows

## Discente: Bernardo de Moura Medeiros
## 13/05/2025

<p> O exercício tem como objetivo principal proporcionar uma experiência prática e guiada com o uso básico do sistema operacional Linux em um ambiente isolado por meio de contêineres Docker. Consolidando o entendimento de comandos essenciais do terminal, no uso do SO Linux. E incentivando uma documentação bem estruturada, afim de aprimorar o gerenciamento e a organização do ambiente. </p>

<br>
<br>

### Inicializando um contêiner Fedora (2.2.1.)

- realizei o comando abaixo para gerar a imagem do fedora:
    ```
    docker run -it --name fedora-tutorial fedora:latest /bin/bash
    ```
**Conclusão - Etapa(2.2.1.):** Foi essencial para a familiarização com a utilização do software Docker Desktop, que disponibiliza imagens Docker dando pull em seus arquivos e funcionalidades e sendo possível rodá-las na minha máquina.

--- 

### Familiarização com comandos de navegação. (2.2.2.)

- realizei o comando abaixo afim de certificar que estou com o superusuário, indicado pelo root:

    ```
    pwd
    ```

- realizei o comando abaixo para acessar o diretório do superuser:

    ```
    cd ~
    ```
    
- realizei o comando abaixo dentro do root, afim de listar as pastas presentes (apesar de não haver alguma):

    ```
    ls
    ``` 

- realizei o comando abaixo como superuser criando o diretório de atividades do curso:

    ```
    mkdir atividades
    ``` 
- acessei o diretório por meio do comando a seguir:

    ```
    cd atividades
    ``` 

- efetuei o comando a seguir para sair do último diretório, nesse caso o atividades, voltando ao dir original do superusuario:

    ```
    cd ..
    ``` 

- testando a instalação de pacotes no fedora, optei por baixar o "clear", para melhor organização do meu ambiente de trabalho, realizado por meio do comando a seguir:

    ```
    dnf install clear
    ``` 

- realizei a limpeza dos comandos anteriores do terminal, a partir do comando a seguir:

    ```
    clear
    ``` 

**Conclusão - (Etapa: 2.2.2.):** Foi possível familiarizar-se com comandos de navegação e manipulação no cmd, via Docker. Tendo algumas adaptações a depender do editor selecionado, que no meu caso foi o Fedora. Comandos como cd, pwd, ls, mkdir e cd .. permitiram a movimentação e organização de diretórios. Todos dos comandos foram abordados em sala de aula, sendo possível realizar e compreende-los com clareza, auxiliando no domínio dos conceitos iniciais de navegação no ambiente Linux.



---

### Manipulação de arquivos, diretórios e subpastas (2.2.3)

- comando efeutado afim de criar um arquivo qualquer, nesse caso txt:

    ```
    touch random_doc.txt
    ```

- realizei o comando abaixo para modificar o nome do arquivo gerado anteriormente:

    ```
    mv random_doc.txt random_doc2.txt
    ```

- com os comandos abaixo, acessei o diretório atividades, criado posteriormente, e dentro criei um novo dir chamado backup:

    ```
    cd atividades
    mkdir backup
    ```

- com o seguinte comando, copiei o arquivo criado na home para a pasta backup:

    ```
    cp ~/random_doc.txt backup/
    ```

- comandos a seguir já contemplados no documento, apenas sinalizando a presença deles para voltar a home do superuser(cd ~) e verificar o local(pwd):

    ```
    cd ~
    pwd
    ```

- comandos a seguir realizado com o objetivo de excluir o documento criado originalmente da home:

    ```
    rm random_doc.txt 
    ```

- efetuei o comando abaixo afim de certificar se o arquivo foi salvo em backup, sendo bem sucedido:

    ```
    Verifique se o arquivo ainda existe em `backup`
    ```

**Conclusão - Etapa (2.2.3.):** As operações realizadas expõem o gerenciamento de arquivos e diretórios no terminal. Foram utilizados comandos essenciais como touch, mv, mkdir, cp, cd, pwd e rm, permitindo a criação, renomeação, cópia, navegação e exclusão de arquivos e pastas. Ao final, foi possível confirmar que o arquivo foi devidamente copiado para o diretório backup, evidenciando o sucesso das ações propostas. A parcela majoritária dos comandos de gerenciamento de pastas e diretórios foram abordados em sala de aula, sendo possível realizar e compreende-los com clareza, auxiliando no domínio da manipulação de arquivos e diretórios no ambiente Linux.

---

### Gerenciamento de pacotes (2.2.4.)

- O comando abaixo, atualiza os pacotes para a versão mais recente do editor (fedora), removendo, atualizando e adicionando arquivos, além de listá-los e expor informações em especifíco sobre cada um, como versão em que ele se encontra, tamanho, tempo de execução dentre outros:

```
    dnf update -y
```

- Instalação do editor nano dentro do fedora, com o comando a seguir:

```
    dnf install nano -y
```

- Verificar a versão do nano, com o comando a seguir:

```
    nano --version
```

- Remoção do editor nano, com o comando a seguir:

```
    dnf remove nano -y
```

**Conclusão - Etapa (2.2.4.):** As operações realizadas são uma breve introdução à manipulação de pacotes. Foram utilizados comandos essenciais no fedora, como update, install, --version e remove, permitindo a visualização de pacotes presentes e atualização dos mesmos, instalação de pacotes específicos, visualização de versão de pacotes específicos e remoção. Ao final, foi possível manipular os pacotes de forma efetiva. As aulas ministradas auxiliaram na instalação de pacotes no editor fedora, via Docker.

--- 

### Permissões de arquivos (2.2.5.)

- O comando a seguir já presente no relato, sendo responsável pela criação de um arquivo:

```
    touch script.sh
```

- O comando a seguir, é responsável em dar permissão(u) de execução ao dono(x):

```
    chmod u+x script.sh
```

- O comando a seguir, lista as permissões vigentes no arquivo:

```
    chmod u+x script.sh
```

**Conclusão - Etapa (2.2.5.):** Nessa etapa rfoi possível compreender como funcionam as permissões de arquivos no Linux, com os comandos chmod u+x e ls -l, para adicionar permissão de execução e manipualação e verificar as permissões vigentes no arquivo, respectivamente, reforçando a ideia de importância da segurança e do controle de acesso no sistema. As aulas ministradas deram uma breve introdução ao chmod, que alterar as permissões de arquivos ou diretórios no Linux, auxiliaram no entendimento dos comandos.

















<p> OBS: todos os comandos foram realizados com o terminal bash. </p>