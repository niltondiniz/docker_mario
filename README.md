# docker_mario
Uma imagem Docker do Super Mario

## Instruções para rodar o jogo no docker

### 1 - Clonando o repositório
#### 1- Crie uma pasta para organizar tudo do seu curso
#### 2- No seu terminal acesse esta pasta usando os comandos de terminal para acessar pastas
#### 3- De dentro da pasta recém criada, digite:
```
git clone https://github.com/niltondiniz/docker_mario.git
``` 
Este comando clona o repositorio que contém as configurações docker para levantar o jogo.
Caso o git peça seus dados, informe de acordo com o solicitado.

#### 4- Agora digite:
```
cd super_mario
```
Este comando entra na pasta referente ao repositório recém baixado

#### 5- Agora vamos "Buildar", ou seja, CONSTRUIR nossa imagem docker do jogo:
```
docker build -t super_mario .
```
Este comando constrói a imagem. O parâmetro -t signfica "Target", ou seja, ALVO. Indicando que minha imagem terá o nome indicado neste parâmetro.
Não se esqueça do ponto no final do comando, significa que eu vou buildar um arquivo Dockerfile que está no mesmo diretório onde eu estou digitando os comandos.

#### 6- Agora nosso ultimo passo, vamos colocar nossa imagem docker (nosso jogo do Mário) pra rodar:
```
docker run -d -p 8600:8080 super_mario
```
Este comando da o start na nossa imagem docker, que nada mais é do que o jogo do Mario encapsulado numa imagem docker, ou seja, num container.

#### 7- Para ver o jogo rodando, basta acessar http://localhost:8600

