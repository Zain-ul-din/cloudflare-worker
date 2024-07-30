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

first time it can take sometime maybe 5 - 10 min to initialize route.

### Enabling CORS

send following fields with response header to tell browser allow CORS.

```js
const corsHeaders = {
	'Access-Control-Allow-Origin': '*',
	'Access-Control-Allow-Methods': 'POST, OPTIONS',
	'Access-Control-Allow-Headers': 'Content-Type',
};
```

check more at,

- [OPTIONS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)
- [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
- [Pre-flight request](https://developer.mozilla.org/en-US/docs/Glossary/Preflight_request)

### AI Gateway

To create AI gateway head over to cloudflare dashboard and create new AI gateway by going to AI tab. They will give us a end point that we can use as a `baseURL` to make calls to OpenAI APIs.

see more at [here](https://developers.cloudflare.com/ai-gateway/).

### Appendix

- [Secrets](https://developers.cloudflare.com/workers/configuration/secrets/#secrets-in-development)
- [OpenAI Worker](https://developers.cloudflare.com/ai-gateway/tutorials/deploy-aig-worker/#3-configure-openai-in-your-worker)
