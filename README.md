# dsa con

> a static web app built with [SvelteKit](https://github.com/sveltejs/kit),
> [felt-ui](https://github.com/feltjs/felt-ui),
> and [Gro](https://github.com/feltjs/gro)

For the purpose of collecting & presenting news & information related to the bi-annual DSA National Convention

deployed:
[dsacon.info](https://dsacon.info)

## running locally

```bash
npx degit feltjs/felt-template cooltoy
cd cooltoy
npm i
# then
npm run dev
# or
gro dev # npm i -g @feltjs/gro
```

To make it your own, change `felt-template` and `template.felt.dev`
to your project name in the following files:

- [`package.json`](package.json)
- [`svelte.config.js`](svelte.config.js)
- [`src/routes/+layout.svelte`](src/routes/+layout.svelte)
- [`src/routes/+page.svelte`](src/routes/+page.svelte)
- update or delete [`src/static/CNAME`](src/static/CNAME)

Then run `npm i` to update `package-lock.json`.

Optionally add a [license file](https://choosealicense.com/)
and [`package.json` value](https://spdx.org/licenses/), like `"license": "MIT"`.

## build

```bash
npm run build
# or
gro build
```

See [Gro's build docs](https://github.com/feltjs/gro/blob/main/src/docs/build.md) for more.

## test

```bash
gro test
gro test filepattern1 filepatternB
gro test -- uvu --forwarded_args 'to uvu'
```

See [uvu](https://github.com/lukeed/uvu),
[`src/lib/example.test.ts`](src/lib/example.test.ts),
and [Gro's test docs](https://github.com/feltjs/gro/blob/main/src/docs/test.md) for more.

## deploy

[Deploy](https://github.com/feltjs/gro/blob/main/src/docs/deploy.md)
(build, commit, and push) to the `deploy` branch, e.g. for GitHub Pages:

```bash
npm run deploy
# or
gro deploy
```

## credits 🐢<sub>🐢</sub><sub><sub>🐢</sub></sub>

[Svelte](https://github.com/sveltejs/svelte) ∙
[SvelteKit](https://github.com/sveltejs/kit) ∙
[Vite](https://github.com/vitejs/vite) ∙
[esbuild](https://github.com/evanw/esbuild) ∙
[uvu](https://github.com/lukeed/uvu) ∙
[TypeScript](https://github.com/microsoft/TypeScript) ∙
[ESLint](https://github.com/eslint/eslint) ∙
[Prettier](https://github.com/prettier/prettier) ∙
[felt-ui](https://github.com/feltjs/felt-ui) ∙
[@feltjs/util](https://github.com/feltjs/util) ∙
[Gro](https://github.com/feltjs/gro)
[svelte-vertical-timeline](https://github.com/K-Sato1995/svelte-vertical-timeline)
& [more](package.json)

## [🐦](https://wikipedia.org/wiki/Free_and_open-source_software)
