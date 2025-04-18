# next-rspack unclear or not displayed css errors

Deps and versions in `package.json`

## Issue

- `example.scss` contains error
- exec `npm run build`
- next start building project
- u see

```
➜  workspace git:(main) ✗ npm run build

> nextjs@0.1.0 build /project/workspace
> next build

   ▲ Next.js 15.3.1 (Rspack)

   Creating an optimized production build ...
 ⚠ `next-rspack` is currently experimental. It's not an official Next.js plugin, and is supported by the Rspack team in partnership with Next.js. Help improve Next.js and Rspack by providing feedback at https://github.com/vercel/next.js/discussions/77800
 ⚠ `next-rspack` is currently experimental. It's not an official Next.js plugin, and is supported by the Rspack team in partnership with Next.js. Help improve Next.js and Rspack by providing feedback at https://github.com/vercel/next.js/discussions/77800
 ⚠ `next-rspack` is currently experimental. It's not an official Next.js plugin, and is supported by the Rspack team in partnership with Next.js. Help improve Next.js and Rspack by providing feedback at https://github.com/vercel/next.js/discussions/77800
 ⚠ Compiled with warnings in 1000ms

⚠ Unexpected token Function("var") at static/css/2cefff9d3ed3ad50.css:0:42

 ✓ Compiled successfully in 2000ms
 ✓ Linting and checking validity of types
 ✓ Collecting page data
 ✓ Generating static pages (5/5)

   ... then i press Ctrl + C
```

- **You don’t understand where the error is or in which file. You only have a hashed file name, and this file doesn’t appear in the `.next` folder.<br/>At the same time, you don’t know its original name in the `src` folder, so you just don’t understand where the error is located at all. Its hard to work this way when u have 1000+ scss files**
- in dev mode `npm run dev` u will not see any errors at all, but its not big issue

## Expected

Something like `Unexpected token Function("var") at src/app/example.scss:3:...`
