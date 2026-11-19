# How this works

There are 2 main parts of the app:

1. renderer: this is the HTML/Javascript-based UI rendered within the Electron container. This runs Vue.js, a React-like Javascript framework for rendering front-end.
2. main: includes the main app (written in Electron). Handles keyboard shortcuts, brings up the UI and overlays.

Note that these 2 both depend on each other, and one cannot run without the other.

# How to develop

The most up-to-date instructions can always be derived from CI:

[.github/workflows/main.yml](https://github.com/SnosMe/awakened-poe-trade/blob/master/.github/workflows/main.yml)

Here's what that looks like as of 2026-08-01.

```shell
cd renderer
npm ci
npm run dev

# In a second shell
cd main
npm ci
npm run dev
```

# How to build

```shell
cd renderer
npm ci
npm run build

cd ../main
npm ci
npm run build
# We want to sign with a distribution certificate to ensure other users can
# install without errors
CSC_NAME="Certificate name in Keychain" npm run package
```

### Packaging on Windows

- `npx electron-builder build --win -p never` (in `main/`, after building `renderer/` and `main/`).
- If packaging fails with *"Cannot create symbolic link : A required privilege is not held by the client"*
  while extracting `winCodeSign`, either enable Windows Developer Mode, or extract the archive once
  by hand (the two macOS symlink errors are harmless):
  `node_modules\7zip-bin\win\x64\7za.exe x -y %LOCALAPPDATA%\electron-builder\Cache\winCodeSign\<id>.7z -o%LOCALAPPDATA%\electron-builder\Cache\winCodeSign\winCodeSign-2.6.0`
- When starting the dev build (`npm run dev`) from a VS Code terminal, clear `ELECTRON_RUN_AS_NODE`
  first, or Electron starts as plain Node and exits. Packaged builds ignore this variable.
