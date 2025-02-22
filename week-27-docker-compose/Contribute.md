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
- start postgres
  - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
- build the image - `docker build -t user-project .`
- Start the image - `docker run -p 3000:3000 user-project`

## Docker Compose installation steps

- Install docker, docker-compose
- Run `docker-compose up`
