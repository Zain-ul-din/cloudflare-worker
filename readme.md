## Cloud Flare Work Deployment Example

This project is created using,

```bash
npm create cloudflare
```

for more checkout this [link](https://developers.cloudflare.com/workers/get-started/guide/)

### Deployment setup

Install `wrangler` cli globally using,

```bash
npm i wrangler -g
```

or you could use,

```bash
npx wrangler
```

It will install wrangler cli temporary.

**Login:**

```bash
npx wrangler login
```

after login verify by running,

```bash
npx wrangler whoami
```

for more checkout [docs](https://developers.cloudflare.com/workers/wrangler/#wrangler).

### Deployment

to run project locally run,

```bash
npx wrangler dev
```

to deploy run,

```bash
npx wrangler deploy
```
