### PROJETO INTEGRADOR 4º SEMESTRE - TaskGo - Grupo 03

    TaskGo é uma plataforma desenvolvida para facilitar a conexão entre clientes e prestadores de serviços locais. O projeto visa resolver um problema comum: a dificuldade em encontrar profissionais confiáveis e disponíveis para tarefas do dia a dia, enquanto muitos trabalhadores autônomos enfrentam barreiras para alcançar novos clientes e expandir sua renda.

## Integrantes do grupo

Henrique Da Rocha Medeiros

Joao Victor Da Silva Caldas

Maria Paula De Oliveira Rodrigues

Mariana Oliveira Mello

Matheus Yoshida Dias

Peterson Fonseca Simiao

Sofia Freire De Andrade Clark

### Observações Técnicas

## Como startar o ambiente de desenvolvimento

# 1) Na pasta onde está o docker-compose.yml e o .env
docker compose up -d db

# 2) Rodar a API (dev)
docker compose up api
# (ou -d para rodar em background)

# 3) (Opcional) Subir o pgAdmin
docker compose --profile tools up -d pgadmin


## Como rodar as migrations
# Abrir um shell no container da API
docker exec -it proxi_api sh

# Dentro do container:
npx prisma generate
npx prisma migrate dev --name init
