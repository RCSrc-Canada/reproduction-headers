This project was created using [Create JD App](https://github.com/OrJDev/create-jd-app)

## Start Dev Server

```bash
pnpm run dev
```

This will start a dev server on port `3000` and will watch for changes.

## Testing Production Build

### Build

```bash
pnpm run build
```

### Start

```bash
pnpm run start
```

This will start a production server on port `3000`.

### Enviroment Variables
You must have all of the following or the server will throw a type error.

- `ENABLE_VC_BUILD`=1
- `DISCORD_ID`=
- `DISCORD_SECRET`=
- `AUTH_SECRET`=b198e07a64406260b98f06e21c457b84
- `AUTH_TRUST_HOST`=true
- `AUTH_URL`=http://localhost:3000
- `UPSTASH_REDIS_REST_URL`=
- `UPSTASH_REDIS_REST_TOKEN`=  

### Deploy to Vercel, check the logs and find....
```
Received new request: /

Unhandled Promise Rejection 	{"errorType":"Runtime.UnhandledPromiseRejection","errorMessage":"ReferenceError: Headers is not defined","reason":{"errorType":"ReferenceError","errorMessage":"Headers is not defined","stack":["ReferenceError: Headers is not defined","    at createHeaders (/var/task/vercel/path0/dist/index.cjs:58588:17)","    at createRequest (/var/task/vercel/path0/dist/index.cjs:58576:14)","    at Object.server [as handler] (/var/task/vercel/path0/dist/index.cjs:58522:17)","    at handler (/var/task/___vc/__launcher.js:53:33)","    at AsyncLocalStorage.run (node:async_hooks:330:14)","    at Server. (/var/task/___vc/__launcher.js:82:28)","    at Server.emit (node:events:513:28)","    at parserOnIncoming (node:_http_server:998:12)","    at HTTPParser.parserOnHeadersComplete (node:_http_common:128:17)"]},"promise":{},"stack":["Runtime.UnhandledPromiseRejection: ReferenceError: Headers is not defined","    at process. (file:///var/runtime/index.mjs:1250:17)","    at process.emit (node:events:525:35)","    at emit (node:internal/process/promises:140:20)","    at processPromiseRejections (node:internal/process/promises:274:27)","    at processTicksAndRejections (node:internal/process/task_queues:97:32)"]}

Unknown application error occurred

Runtime.Unknown
```
