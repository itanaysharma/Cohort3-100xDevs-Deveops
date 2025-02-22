## Manual installation

- Install nodejs locally ()
- clone the repo
- install dependencies (npm install)
- start the DB locally
  - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
  - Go to neon.tech and get youself a new db
- change .env file and update your db creds
- npx prisma migrate
- npx prisma genarate
- npm run build
- npm run start

## Docker installation

- Install docker
- Create a network - `docker network create user_project`
- start postgres
  - docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
- build the image - `docker build --network=host -t user-project .`
- Start the image - `docker run -e DATABASE_URL=postgresql://postgres:mysecretpassword@postgres:5432/postgres --network user_project -p 3000:3000 user-project`

## Docker Compose installation steps

- Install docker, docker-compose
- Run `docker-compose up`
