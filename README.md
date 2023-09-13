This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

The command i used are 

```bash
bunx create-next-app <project-name> --ts --tailwind --eslint --app --src-dir --use-bun --import-alias "@/*"
```

Thanks to [ericklarsen](https://github.com/oven-sh/bun/issues/4664#issuecomment-1712570408) for the solution

### But there is still a problem
```
user@wsl:~/test/next-with-bun$ bun run dev
$ next dev
- ready started server on localhost:3000, url: http://localhost:3000
- event compiled client and server successfully in 407 ms (20 modules)
- wait compiling...
- event compiled client and server successfully in 53 ms (20 modules)
- wait compiling /page (client and server)...
- event compiled client and server successfully in 5s (426 modules)
- wait compiling...
- event compiled successfully in 277 ms (235 modules)
ConnectionClosed: The socket connection was closed unexpectedly. For more information, pass `verbose: true` in the second argument to fetch()
 path: "http://localhost:42351/"

- wait compiling /_error (client and server)...
ConnectionRefused: Unable to connect. Is the computer able to access the url?
 path: "http://localhost:42351/favicon.ico"

ConnectionRefused: Unable to connect. Is the computer able to access the url?
 path: "http://localhost:42351/"

TimeoutError: The operation timed out

TimeoutError: The operation timed out
```

WHAT DOES IT MEAN?!?! WHY I CAN'T OPEN LOCALHOST:3000 FROM MY BROWSER?!?! "Internal Server Error" is all it said  

runing using ```bunx --bun next dev``` also show the same

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
