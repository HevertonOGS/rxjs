
# Typescript Starter Project

This is a Typescript project to use to initialize the development into a new project.

---

## Create Project

To create the same project you can follow the steps:

1. Create and access the project directory:

```mkdir typescript-starter```\
```cd typescript-starter```

1. Setup Node.js package.json:

```npm init -y```

3. Add TypeScript as a dev dependency:

```npm install typescript --save-dev```

4. Install ambient Node.js types for TypeScript:

```npm install @types/node --save-dev```

5. Create a tsconfig.json:

```npx tsc --init --rootDir src --outDir build --esModuleInterop --resolveJsonModule --lib es6 --module commonjs --allowJs true --noImplicitAny true```

6. Create the src folder and create our first TypeScript file:

```mkdir src```\
```touch src/index.ts```\
```console.log('Hello world!')```

7. Compiling our TypeScript:

```npx tsc```

### Useful configurations & scripts

1. Cold reloading:

```npm install --save-dev ts-node nodemon```

2. Add a nodemon.json config:

```
{
  "watch": ["src"],
  "ext": ".ts,.js",
  "ignore": [],
  "exec": "ts-node ./src/index.ts"
}
```

3. Install rimraf:

```npm install --save-dev rimraf```

4. Add scripts on package.json:

```"start:dev": "nodemon"```\
```"build": "rimraf ./build && tsc"```\
```"start": "npm run build && node build/index.js"```