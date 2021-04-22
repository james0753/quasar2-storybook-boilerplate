# Quasar2 Storybook Boilerplate

Quasar2 Storybook Boilerplate

## Prerequisition

- node 14, npm, android studio, xcode

```bash
npm install -g cordova @quasar/cli @quasar/icongenie
yarn
cd src-cordova
cordova requirements
```

### Start the app in development mode (hot-code reloading, error reporting, etc.)

```bash
yarn run dev:browser
yarn run dev:android
yarn run dev:ios
```

### storybook

```bash
yarn run dev:storybook
yarn run build:storybook
```

### Lint the files

```bash
yarn run lint
```

### Unit Test

```bash
yarn run test:unit:ci
```

### E2E Test - Not Yet Fixed

```bash
yarn run test:e2e:ci
```

### Audit - Not Yet Fixed

```bash
yarn run audit:snyk
yarn run audit:node_modules
yarn run audit:licenses
yarn run audit:lighthouse
```

- `yarn run audit:snyk` needs running `./node_modules/.bin/snyk auth` first

### Build the app for production

```bash
yarn run build:android
yarn run build:ios
```

### key signing - Change to your keystore

```bash
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore <your-release-key.keystore> \dist\cordova\android\apk\release\android-debug.apk alias_name
```

### Documents

- ADR : `doc/architecture/decisions`

### Cautions

- DO NOT Upgrate to webpack5 : quasar does not support webpack5 yet

### Troubleshooting

- TLS error while yarn  `set NODE_TLS_REJECT_UNAUTHORIZED=0`, `$env:NODE_TLS_REJECT_UNAUTHORIZED=0`
