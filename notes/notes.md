# Notes

## Setup

### Install Dependencies

Create next app with Typescript 

```sh
npx create-next-app --ts
```

Run

```sh
npm run dev
```

Install types for node

```sh
npm i -D @types/node
```

Install MUI

```sh
npm i @mui/material @emotion/react @emotion/styled --legacy-peer-deps
```

Install Roboto font using npm

```sh
npm i @fontsource/roboto
```

Them import into the entry point 

```ts
import '@fontsource/roboto/300.css';
import '@fontsource/roboto/400.css';
import '@fontsource/roboto/500.css';
import '@fontsource/roboto/700.css';
```

Font icons

```sh
npm i @fontsource/material-icons @fontsource/material-icons-rounded @fontsource/material-icons-outlined @fontsource/material-icons-sharp @fontsource/material-icons-two-tone
```

Installation

```ts
import "@fontsource/material-icons";
import "@fontsource/material-icons-rounded";
import "@fontsource/material-icons-outlined";
import "@fontsource/material-icons-sharp";
import "@fontsource/material-icons-two-tone";
```

SVG icons

```sh
npm i @mui/icons-material --legacy-peer-deps
```


#### Resources

- [Installation - MUI](https://mui.com/getting-started/installation/)
- [React Typography component - MUI](https://mui.com/components/typography/#install-with-npm)
- [@fontsource/roboto](https://www.npmjs.com/package/@fontsource/roboto)
- [Fontsource | Material Icons](https://fontsource.org/docs/icons/material-icons)
- [Fontsource | Next.js](https://fontsource.org/docs/guides/nextjs)

    ```tsx
    import "@fontsource/open-sans/400.css";
    import "@fontsource/open-sans/700.css";

    function MyApp({ Component, pageProps }) {
    return <Component {...pageProps} />;
    }

    export default MyApp;
    ```

## File Structure

Make a `src` folder 

Move the `pages` and `styles` folder into the `src` folder.

```sh
mkdir src && mv pages/ src/ && mv styles/ src/
```

## Absolute Imports

[Absolute Imports and Module path aliases](https://nextjs.org/docs/advanced-features/module-path-aliases)

The `baseUrl` configuration option allows you to import directly from the root of the project.

```json
// tsconfig.json or jsconfig.json
{
  "compilerOptions": {
    "baseUrl": "."
  }
}
```

```js
// components/button.js
export default function Button() {
  return <button>Click me</button>
}

// pages/index.js
import Button from 'components/button'

export default function HomePage() {
  return (
    <>
      <h1>Hello World</h1>
      <Button />
    </>
  )
}
```

## MUI NextJs with TypeScript example

[Next.js with TypeScript example](https://github.com/mui/material-ui/tree/master/examples/nextjs-with-typescript)

[Emotion - Styled Components](https://emotion.sh/docs/styled)