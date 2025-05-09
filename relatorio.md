# Relátorio - Atividade 02 - utilizando linux no windows

<p> OBS: todos os comandos foram realizados com bash </p>

- realizei o comando abaixo para gerar a imagem do fedora:
    ```
    docker run -it --name fedora-tutorial fedora:latest /bin/bash
    ```

- realizei o comando abaixo afim de certificar que estou com o superusuário, indicado pelo root:

    ```
    pwd
    ```
    
- realizei o comando abaixo dentro do root, afim de listar as pastas presentes (apesar de não haver alguma):

    ```
    ls
    ``` 