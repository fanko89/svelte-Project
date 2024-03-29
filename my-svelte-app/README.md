# overview of the different sections of my Invoice code:
---


## Dependencies
---

styles.css: a stylesheet for styling the invoice form

onMount and svelte: libraries used for handling the mounting of the invoice form

jsPDF: a library for creating PDFs

html2canvas: a library for capturing screenshots of HTML elements

SignaturePad: a library for capturing and storing signatures

## Variables
---

signaturePad: a variable used to store a signature captured by the SignaturePad library

yourTotal: a variable used to store the total cost of the items listed in the invoice

yourAmountDue: a variable used to store the amount due after subtracting any payments made

inputHeight: a variable used to store the height of the input fields in the invoice form

paidElement: a variable used to store the payment element in the invoice form

rows: an array of objects representing the rows in the invoice form, including name, description, cost, quantity, and price

## Functions
---

clearSignature(): a function used to clear the captured signature

saveSignature(): a function used to save the captured signature

getPDF(): a function used to create a PDF of the invoice form

resizeInput(): a function used to resize the input fields in the invoice form

getCurrentDate(): a function used to get the current date

updatePrice(): a function used to update the price of an item in the invoice form based on its quantity and cost

updateTotal(): a function used to update the total cost of the items in the invoice form

updateBalance(): a function used to update the balance due after subtracting any payments made

addRow(): a function used to add a new row to the invoice form

removeRow(): a function used to remove a row from the invoice form






---

# svelte app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:8080](http://localhost:8080). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

If you're using [Visual Studio Code](https://code.visualstudio.com/) we recommend installing the official extension [Svelte for VS Code](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode). If you are using other editors you may need to install a plugin in order to get syntax highlighting and intellisense.

## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```

## Using TypeScript

This template comes with a script to set up a TypeScript development environment, you can run it immediately after cloning the template with:

```bash
node scripts/setupTypeScript.js
```

Or remove the script via:

```bash
rm scripts/setupTypeScript.js
```

If you want to use `baseUrl` or `path` aliases within your `tsconfig`, you need to set up `@rollup/plugin-alias` to tell Rollup to resolve the aliases. For more info, see [this StackOverflow question](https://stackoverflow.com/questions/63427935/setup-tsconfig-path-in-svelte).

## Deploying to the web

### With [Vercel](https://vercel.com)

Install `vercel` if you haven't already:

```bash
npm install -g vercel
```

Then, from within your project folder:

```bash
cd public
vercel deploy --name my-project
```

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
