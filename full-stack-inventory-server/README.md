## Prisma commands

Init the database and Prisma
```bash
npx prisma init
```

Generate the client
```bash
npx prisma generate
```

Migrate the database
```bash
npx prisma migrate dev --name init
```

Seed the database
```bash
npm run seed
```

## Typescript configuring

Install typescript
```bash
npm install --save-dev typescript
```

Initialize typescript
```bash
npx tsc --init
```

Install packages for node and typescript
```bash
npm i --save-dev ts-node @types/node
```

Add scripts to package.json
```json
{
  "scripts": {
    "seed": "ts-node prisma/seed.ts",
    "build": "rimraf dist && npx tsc",
    "start": "npm run build && node dist/index.js",
    "dev": "npm run build && concurrently \"npm tsc -w\" \"nodemon --exec ts-node src/index.ts\""
  }
}
```


