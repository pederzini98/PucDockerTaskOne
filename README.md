# Estrutura de Docker Compose para Jogo de Adivinhação

Este projeto implementa uma infraestrutura com Docker Compose para orquestrar os serviços necessários para rodar o jogo de adivinhação.

## Componentes
- **Backend**: API Flask para o jogo.
- **Frontend**: Aplicação React servida pelo NGINX.
- **Banco de Dados**: Postgres para armazenar os dados do jogo.


1. Configure o `.env`:
   ```env
   DATABASE_URL=postgresql://user:password@db:5432/guess_game
   SECRET_KEY=your_secret_key
   ```

2. Inicie os containers:
   ```bash
   docker-compose up --build
   ```

3. Acesse os serviços:
   - Frontend: [http://localhost](http://localhost)
   - Backend: [http://localhost/api](http://localhost/api)

## Atualização
Para atualizar qualquer serviço, altere o Dockerfile correspondente ou troque a imagem no `docker-compose.yml` e execute:
```bash
docker-compose up --build
```

## Persistência de Dados
Os dados do Postgres são armazenados em um volume chamado `db_data`.

---
