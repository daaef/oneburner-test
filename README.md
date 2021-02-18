# Parcel Boilerplate

This is a boilerplate for a static website using the Parcel bundler. This boilerplate uses Parcel 1. Comes with Babel (uses `preset-env`), ESLint (uses Airbnb's styleguide as a base), Prettier, Autoprefixer, Sass, and posthtml-include for HTML partials. I've also included my VSCode settings so you can get nice code linting and formatting right in your editor if you'd like. See notes below for details.

## Usage

**1) Clone this repo**

**2) Install dependencies**

```

npm i

```

**3) Start server and start building**

```

npm start

```

When you're ready to launch for production:

```

npm run build

```

## Babel Note

There is no `.babelrc` because Parcel transpiles JS with Babel using `preset-env` by default. If you want to change the Babel config, check out [Parcel's docs](https://parceljs.org/javascript.html).

## HTML Partials

Put partials in `src/html/partials` and include them with `<include src="partial-name.html"></include>`. The current directory referenced within relative URL paths within partials is the directory containing the file that included the partial.

## ESLint and Prettier integration with VS Code

I've included the VS Code settings I use to automatically lint and format my projects. You can find them in `.vscode/settings.json`. You can use these settings as is, or as a jumping off point. They should automatically apply if you open the root of this project in VS Code. If you'd rather not use them, delete the `.vscode` folder.

In order for these settings to work properly, you'll need to install the following two extensions:

1. [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
2. [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

An important thing to note with my setup is that I run Prettier through ESLint, using ESLint's formatter for JS files. This is why the default Javascript validator and formatter that come with VSCode are disabled. I use Prettier directly to format everything else.

You can alter the Prettier and ESLint settings to your liking in their respective config files (`.prettierrc.json` and `.eslintrc.json`). Prettier rules within `.eslintrc.json` are for JavaScript files only, and rules within `.prettierrc.json` are for all other files.
