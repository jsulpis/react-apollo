# React & Apollo Tutorial

This is the sample project that belongs to the [React & Apollo Tutorial](https://www.howtographql.com/react-apollo/0-introduction/) on How to GraphQL.

*This fork has a few modifications compared to the original repository. The local postgres database and the prisma server are already configured in `docker-compose.yml` to make it easier to get started with.*

## How to use

### 1. Clone repository

```sh
git clone https://github.com/jsulpis/react-apollo/
```

### 2. Install dependencies & Deploy the Prisma database API

To install the Prisma CLI globally with Yarn, use the following command:
```sh
yarn global add prisma
```

Also, run the following commands:
```sh
cd react-apollo/server
yarn install
```

Then, run Prisma locally via Docker:

1. Ensure you have Docker installed on your machine. If not, you can get it from [here](https://store.docker.com/search?offering=community&type=edition).
1. Run `docker-compose up -d`
1. Run `prisma deploy`

### 3. Start the server

To start the server, all you need to do is execute the `start` script by running the following command inside the `server` directory:

```sh
yarn start
```

> **Note**: If you want to interact with the GraphQL API of the server inside a [GraphQL Playground](https://github.com/prisma/graphql-playground), you can navigate to [http://localhost:4000](http://localhost:4000).

> **Alternatively**, there is a `graphiql.html` file in the root folder that you can just open in a browser and you will have a ready-to-use GraphiQL IDE pointing to `http://localhost:4000`.

### 4. Run the app

Now that the server is running, you can start the React app as well. The commands need to be run in a new terminal tab/window inside the directory `client` (because the current tab is blocked by the process running the server):

```sh
yarn install
yarn start
```

You can now open your browser and use the app on [http://localhost:3000](http://localhost:3000).
