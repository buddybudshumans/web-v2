<center>
    <img src="card.png" style="display: block; margin-left: auto; margin-right: auto; width: 300px;"></img>
    <h1 style="color: #32ae62;">Terbium v2</h1>
</center>

## <span style="color: #32ae62;">Some of the technologies used</span>

- [Vite](https://vite.dev)
- [React](https://react.dev)
- [TailwindCSS](https://tailwindcss.com)
- [FilerJS](https://github.com/filerjs/filer)
- [Fflate](https://github.com/101arrowz/fflate/)
- [BareMux](https://github.com/mercuryworkshop/bare-mux)

## <span style="color: #32ae62;">Features</span>

- All new UI
- A Dynamic Shell
- Better Window Manager
- A desktop
- App Store
- A brand new terminal
- Anura Compatability layer (Liquor)
- Electron Compatability layer (Lemonade)
- And lots more!

## <span style="color: #32ae62;">Setup</span>

> <span style="font-family: url('https://fonts.googleapis.com/css2?family=Roboto&display=swap'); color: #ffd900;">⚠</span> <span style="color: #ffd900;">NOTE:</span> Terbium **WILL NOT** build on versions of Node older than version 20.

To get started it's pretty easy, you need either npm, or pnpm, which can be installed by running: `npm i -g pnpm` and then you just need to the run following command:

```bash
pnpm i && pnpm start # Replace pnpm with npm if your not going to use pnpm
```

and visit [http://localhost:3000](http://localhost:3000) you should be good to go!

If you are developing/modifying terbium you can just run `pnpm run dev`, **DO NOT** use the development server for Production use. Instead, just run `pnpm start`. For any further backend configuration visit the `.env` file to configure the backend a bit.

> <span style="font-family: none; color: #ffd900;">⚠</span> <span style="color: #ffd900;">Warning</span><br>
> If you are going to static host Terbium, you will need to change the wisp server, and you would need to follow those steps. Refer to this [document](./docs/static-hosting.md) for more information.

### <span style="color: #32ae62;">Documentation</span>

If you wish to develop or just learn more about Terbium's components and stuff, feel free to read our [Documentation](/docs/README.md)

If you're looking to see what Anura APIs and features are supported in terbium, refer to: [here](/docs/anura-compat.md), if you're looking to see what Electron API's are supported in terbium refer to: [here](/docs/lemonade-compat.md)

### <span style="color: #32ae62;">Contributors</span>

- [SNOOT](https://github.com/NovaAppsInc)
- [XSTARS](https://github.com/Notplayingallday383)
- [illusionTBA](https://github.com/illusionTBA)
- [Rafflesia](https://github.com/ProgrammerIn-wonderland)
- [Riftriot](https://github.com/Riftriot)
- [ironswordX](https://github.com/ironswordX)
- [Ryan](https://github.com/MovByte)

Licensed under the [**AGPL3 License**](https://www.gnu.org/licenses/agpl-3.0.en.html)

## Hosting / Deploying (GitHub Pages)

This repository includes a GitHub Actions workflow that automatically builds and deploys the production `dist/` output to GitHub Pages when you push to `main`.

Quick checklist before deploying:

- Ensure `vite.config.ts` has `base` set to your repo path if you're hosting as a project site, for example:

```ts
// vite.config.ts
export default defineConfig({
    base: '/web-v2/', // change if your repo name or hosting path differs
    // ...
})
```

- Verify `public/404.html` exists (the project already contains one) so client-side routing works on Pages.

How the automatic deploy works:

- The workflow file is at `.github/workflows/pages.yml`.
- On push to `main` the action installs dependencies, runs `npm run build`, uploads `dist/` and publishes it to GitHub Pages.

To test locally before pushing:

```bash
# install deps
npm install

# build production assets
npm run build

# preview the built site
npm run preview
# or
npx serve dist
```

To trigger the deploy (push to main):

```bash
git add .
git commit -m "chore: prepare site for GitHub Pages"
git push origin main
```

If you'd like a one-shot deploy (instead of Actions) we can add `gh-pages` scripts and a `deploy` command — tell me if you prefer that.
