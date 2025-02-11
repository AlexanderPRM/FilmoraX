![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/AlexanderPRM/FilmoraX/linters.yaml)
![License](https://img.shields.io/github/license/AlexanderPRM/FilmoraX.svg)
![GitHub repo size](https://img.shields.io/github/repo-size/AlexanderPRM/FilmoraX)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/AlexanderPRM/FilmoraX)
![GitHub Release](https://img.shields.io/github/v/release/AlexanderPRM/FilmoraX)

# FilmoraX

Repository for the development of a FilmoraX project, which is an online cinema. Project consists of several microservices, which collectively provide functionality of online cinema.

The development is conducted according to the principle of clean architecture.

Following microservices are user in the project.

- Auth microservice with JWT Tokens (In develop).
- Microservice which work with movies (Planned).
- Microservice which for with UGC, for example, likes, reviews (Planned).
- Billing microservice (Planned).
- Notifications microservice, for example, sending emails to users (Planned).


As a API Gateway is used Nginx. If verification is required, Nginx send request to Auth microservice and if response is okay, go next.

Each microservice directory has a two README files on english and russian with detailed description of microservice work.

## How start a project?

Each microservice have two files:

```bash
[microservice_name]
   ├── .env.example
   ├── .env.prod.example
```

For start you need remove .example extension, file .env used for develop, and file .env.prod for production. If you want launch project in production mode, please fill the variables in file .env.prod

Every microservice use Sentry for logging, please fill DSN in env files if you want use them. [**Landing of technology**](https://sentry.io/)

Project root has ./start.sh file written in Bash.
It contains commands for start the project.

```bash
# Start project in develop mode.
./start.sh --type=develop

# Start project in production mode.
./start.sh --type=production
```

Project require Docker for start - [**Installation manual**](https://docs.docker.com/manuals/)
