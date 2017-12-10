# Javascript

## Using a boilerplate

### Set up

Create-react-app automatically includes webpack, Babel, Autoprefixer, ESLint, Jest (but they are hidden).

If using create-recat-app for the first time:
```
npm install -g create-react-app
```

```
create-react-app <app-name>
cd <app-name>
yarn start
```

Then open http://localhost:3000/ to see your app.

### Ejecting from the transitive dependencies

Running `yarn run eject` copies all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. It's permanent!

## Cutom set up

### Webpack

yarn add webpack webpack-dev-server --dev

```
// webpack.config.js

module.exports = {
  entry: "./src/app.js",
    output: {
      filename: "dist/bundle.js"
    }
  }
}
```

```
// package.json
"scripts": {
  "start": "webpack-dev-server --open"
}
```

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <script src="dist/bundle.js"></script>
  </body>
</html>
```

### Babel

```
yarn add babel-loader babel-core babel-preset-env --dev
```

```
// webpack.config.js
module.exports = {
  // ...
  module: {
    rules: [
      {
        test: /\.js$/,
        include: "/src/",
        use: {
          loader: "babel-loader",
          options: {
            presets: [ "env" ]
          }
        }
      }
    ]
  }
  // ...
}
```

### ESLint

```
yarn add eslint --dev
```

You can initialise an eslint configuration file (generally .eslintrc) by running the following:
```
./node_modules/.bin/eslint --init
```

### Browserlist

```
// package.json
{
  "browserslist": [
    "> 1%",
    "last 2 versions"
  ]
}
```

### Typescript

For Typescript and Webpack to play nicely together:
```
yarn add typescript awesome-typescript-loader source-map-loader --dev
```

Create a tsconfig.json

### Semantic UI

```
yarn add semantic-ui-react
```
