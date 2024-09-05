NAVIGATION
[1. GETTING STARTED](#getting-started)

[3. DEPLOY ON VERCEL](#deploy-on-vercel)

[4. NEXT-INTL RULES](#next-intl-messages-rules)
## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
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

## NEXT-INTL MESSAGES RULES
Message files of next-intl should follow the rules so it can be easy to search and maintainable

This is the structure of json file
```
|
|__"common"
|   |_ ...words that appear frequently in other files (e.g: add, save, delete, edit, cancel, register,...)
|   |_"form"
|   | |_ "placeholder": {... common placeholders in forms (e.g: name, email, ...)}
|   |
|   |_"error": ...common validate error messages
|       
|__"navigation": ...items in navigation components (menu, sidebar, topbar ...)
|
|__[page]:
|   |_...words of the page need to be translated
|   |_"form"
|   | |_"title":
|   | | |_"new": title for new form
|   | | |_"edit": title for edit form
|   | |
|   | |_ "placeholder": ... placeholders in forms of the page
|   | 
|   |_"error": ... validate error messages of the page
|   |_"alert": ...alert messages of the page
|   |_"message": ... fetch messages of the page
|
|
```