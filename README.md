# Projeto Docker Todo List desenvolvido na Trybe.
# Observação: O front end foi desenvolvido pela Trybe, no front trabalhei somente com a configuração do docker.

## Requisitos para desenvolvimento do projeto:
### 1. Crie um container em modo interativo, sem rodá-lo, nomeando-o como `01container` e utilizando a imagem `alpine` na versão `3.12`

### 2. Inicie o container `01container`

### 3. Liste os containers filtrando pelo nome `01container`

### 4. Execute o comando `cat /etc/os-release` no container `01container` sem se acoplar a ele

### 5. Remova o container `01container`

### 6. Faça o download da imagem `nginx` com a versão `1.21.3-alpine` sem criar ou rodar um container

### 7. Rode um novo container com a imagem  `nginx` com a versão `1.21.3-alpine` em segundo plano nomeando-o como `02images` e mapeando sua porta padrão de acesso para porta `3000` do sistema hospedeiro

### 8. Pare o container `02images` que está em andamento

### 9. Gere uma build a partir do Dockerfile do `back-end` do `todo-app` nomeando a imagem para `todobackend`

### 10. Gere uma build a partir do Dockerfile do `front-end` do `todo-app` nomeando a imagem para `todofrontend`

### 11. Gere uma build a partir do Dockerfile dos `testes` do `todo-app` nomeando a imagem para `todotests`
# Requisito bônus do projeto

## Docker-compose

### 12. Suba uma orquestração em segundo plano com o docker-compose de forma que `backend`, `frontend` e `tests` consigam se comunicar


##### front-end

- O container de `todofrontend` deve rodar na porta `3000`;
- O nome do _service_ deverá ser `todofront`;
- Deve ter como dependencia o container `backend`;
- Deve ter uma variável de ambiente `REACT_APP_API_HOST` que recebe como valor o nome do container do `backend`.
  - Lembrando que, dentro de uma rede docker, o host de um container é indentificado pelo seu nome.

##### back-end

- O container de `todobackend` deve rodar na porta `3001`;
- O nome do _service_ deverá ser `todoback`;
