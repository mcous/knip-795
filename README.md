# Knip gitignore bug

Re: webpro-nl/knip#795

## Setup

```shell
gh clone mcous/knip-795
cd knip-795
pnpm install
```

## Reproduction

[gitignore](./.gitignore) contents:

```gitignore
node_modules
*#
```

Run:

```shell
pnpm knip              # knip erroneously reports no unused files
pnpm knip:no-gitignore # knip correctly reports `src/not-used.js`
```
