# Statsig Node Server SDK - Edge Config Adapter
[![npm version](https://badge.fury.io/js/statsig-node-vercel.svg)](https://badge.fury.io/js/statsig-node-vercel) 

A first party Edge Config integration with the [Statsig server-side Node.js SDK](https://github.com/statsig-io/node-js-server-sdk).

## Quick Setup
1. Install the Statsig Node SDK
```
npm install statsig-node@5.3.0
```
2. Install this package
```
npm install statsig-node-vercel
```
3. Install the [Statsig Vercel Integration](https://vercel.com/integrations/statsig)
4. Import the package
```
import { EdgeConfigDataAdapter } from 'statsig-node-vercel'
```
5. Create an instance of the `EdgeConfigDataAdapter`
```
const dataAdapter = new EdgeConfigDataAdapter('KEY_FROM_INSTALLATION');
```
6. When initializing the `statsig` sdk, add the adapter to options
```
await statsig.initialize(
    'server-secret-key',
    { dataAdapter: dataAdapter },
);
```
