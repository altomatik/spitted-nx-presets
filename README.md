# nx-preset-files

This is a dump (spit) of generated files from create-nx-workspace for all
the presets as of 14-Jul-2023.

The presets are:

```js
["apps", "empty", "core", "npm", "ts",
"web-components", "angular-monorepo", "angular-standalone",
"react-monorepo", "react-standalone", "next", "nextjs-standalone",
"react-native", "expo", "nest", "express", "react",
"angular", "node-standalone", "node-monorepo", "ts-standalone"]
```

Files generated using this pattern:

```
pnpm create nx-workspace@latest \
    --skipGit=false \
    --nxCloud=false \
    --appName=hello \
    --preset=${PRESET_NAME} \
    --name=${PRESET_NAME}
```

For `node-monorepo` and `node-standalone` preset, must pass `--framework`
option. Accepted values are: `express`, `koa`, `fastify`, `nest`, `none`.

For `react`, `angular` preset, it will expands to `**-standalone` or
`**-monorepo` variant by prompting it.

Filled prompt for some of the presets are below.

`angular-monorepo`, `angular-standalone`:

```
✔ Default stylesheet format · css
✔ Would you like to use Standalone Components in your application? · No
✔ Would you like to add routing? · Yes
```

`react-monorepo`, `react-standalone`:

```
✔ Which bundler would you like to use? · vite
✔ Default stylesheet format · css
```

`next`, `nextjs-standalone`:

```
✔ Would you like to use the App Router (recommended)? · Yes
✔ Default stylesheet format · css
```

`node-standalone`, `node-monorepo`, `express`, `nest`':

```
✔ Would you like to generate a Dockerfile? [https://docs.docker.com/] · Yes
```
