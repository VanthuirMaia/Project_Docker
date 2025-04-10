# Iniciar contêiner PostgreSQL

docker run --name postgres-dados -e POSTGRES_PASSWORD=segredo -e POSTGRES_USER=analista -e POSTGRES_DB=datawarehouse -p 5432:5432 -d postgres:14.8

# Verificar status do contêiner

docker ps

# Executar o cliente psql dentro do contêiner

docker exec -it postgres-dados psql -U analista -d datawarehouse

# No exemplo isolado, o banco começa vazio

# No Docker Compose, será preenchido com dados iniciais e através da API

# Parar o contêiner

docker stop postgres-dados

# Reiniciar o contêiner

docker start postgres-dados
