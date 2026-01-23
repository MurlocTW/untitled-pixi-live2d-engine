## Cloning the repo

#### Cloning via SSH

```sh
git clone git@github.com:Untitled-Story/untitled-pixi-live2d-engine.git --recursive
```

#### Cloning via HTTPS

```sh
git clone https://github.com/Untitled-Story/untitled-pixi-live2d-engine.git --recursive
```

If you already cloned without submodules:

```sh
git submodule update --init --recursive
```

## Setup

Install dependencies (pnpm is recommended, but npm works too):

```sh
pnpm install
# or
npm install
```

Download Live2D core files into `./Core`:

```sh
npm run setup
```

## Build and checks

Create production bundles:

```sh
npm run build
```

Generate bundled type definitions:

```sh
npm run type
```

Run lint + typecheck:

```sh
npm run check
```

## Playground

The playground is for debugging and testing. To run the playground:

```sh
npm run playground
```

Then make changes to `playground/index.ts` and check the result.

Changes to this file should _not_ be committed to git. You can run this command to tell git not to track this file:

```sh
git update-index --skip-worktree playground/index.ts
```

Cancel Mark

```sh
git update-index --no-skip-worktree playground/index.ts
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any ideas or suggestions.

Before contributing, or better yet, before each commit, please run:

```sh
npm run lint:fix
```

If there are any errors that cannot be fixed automatically, please fix them manually.
