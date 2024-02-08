# CloudBeat integration example for Playwright-NodeJS

Add CB package to your project:

`npm i @cloudbeat/playwright`.

Modify `playwright.config.ts` to use CB reporter:

```javascript
export default defineConfig({
  ...
  reporter: process.env.CB_AGENT ? '@cloudbeat/playwright' : 'html',
  ...
}

```

 `CB_AGENT` environment variable can be used to determine whether we are running from CB context or not. It is set to `true` on CB execution agents and should **not** be present on developer's machines.