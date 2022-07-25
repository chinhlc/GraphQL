## Install NestJS CLI

```bash
npm i -g @nestjs/cli
```

# Create a new project

```bash
nest new nestjs-graphql

cd nestjs-graphql
```


# Install required libraries

```bash
npm i --save @nestjs/graphql graphql-tools graphql

npm i --save class-validator apollo-server-express
```

# Create a .graphql and generate the code
- Lệnh 'tsc' để từ file *.ts nó sẽ tạo ra file *.js
- Lệnh 'node' để từ file *.graphql nó sẽ tạo ra file graphql.ts theo config trong file generate-typings.js

```bash
tsc src/generate-typings.ts

node src/generate-typings.js
```

# Run the application

```bash
npm run start
```
http://localhost:3000/graphql


# Mutations

```graphql
mutation createVideo {
  createVideo(
    input: { title: "Video 1", url: "https://you.tube/vid-1", userId: "1" }
  ) {
    id
    title
    url
    author {
      id
      name
    }
  }
}
```

# Queries

```graphql
query videos {
 videos {    
    id
    title
    url
    author {
      id
      name
    }
  }
}
```
