docker run --name Postgres -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres

CREATE USER docker with password 'docker';
CREATE DATABASE nodeauth;
GRANT ALL PRIVILEGES ON DATABASE nodeauth TO docker;

yarn init -y
yarn add express
yarn add sequelize pg
yarn add sequelize-cli -D
yarn add nodemon -D
yarn add jest -D
yarn add sqlite3 -D
yarn jest --ini
yarn sequelize init
yarn sequelize migration:create --name=create-users
yarn add dotenv
yarn add supertest -D
yarn add bcryptjs
yarn add jsonwebtoken
yarn add factory-girl
yarn add faker -D