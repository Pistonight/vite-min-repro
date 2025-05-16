# vite-min-repro

Minimal reproduction of issues with Vite/Vitest

## Drive letter casing issue

Reproed on node version `22.14`, `22.15` and `24.0`

Repro steps:
1. Open command prompt
1. Set the debug flag `set DEBUG=vite-tsconfig-paths:resolve`
1. Switch to upper case drive letter `cd C:\path\to\repo`
1. `npm install` ( delete `node_modules` if fails)
1. `npm run build`
1. Build is successful
1. Switch to lower case drive letter `cd c:\path\to\repo`
1. `npm run build` - fails
1. Switch to upper case drive letter `cd C:\path\to\repo`
1. `npm run build` - successful

