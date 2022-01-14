# Realtime Collaborative IDE

A realtime collaborative IDE with code execution, input/output, and built-in USACO submissions. Designed primarily for Competitive Programming and USACO, with mobile support for coding on the go.

## Running Locally

This project uses the [Firebase Realtime Database](https://firebase.google.com/docs/database). [This tutorial](https://firebase.google.com/codelabs/firestore-web) is helpful (even though Cloud Firestore is not what's being used here). You'll need to install the [firebase CLI](https://firebase.google.com/docs/cli#install_the_firebase_cli) and [Yarn](https://classic.yarnpkg.com/en/docs/install).

```
yarn install
firebase emulators:start
yarn dev
```

### Configuring Firebase

You can update the Firebase configuration (if you want to use a custom firebase project, for example) by modifying `src/components/WorkspaceInitializer.tsx`. There, you can also set `shouldUseEmulator` to `false` if you don't want to use the firebase emulator.

## Tech Stack

- Code execution supported through [Judge0](https://judge0.com/)
- Realtime collaboration with [Firepad](https://firepad.io/)
- Monaco Editor
- React
- Jotai
- Vite
- Typescript
- Tailwind CSS
- Firebase Realtime Database
- Jest and Playwright for end-to-end testing
- Deployed with Vercel

## Contact Info

If you have any questions, please open an issue or reach out to us at teamnexustech@gmail.com.

## Misc Notes

### Firepad Browser Incompatibility ([firepad#315](https://github.com/FirebaseExtended/firepad/issues/315))

### Enabling Playwright Debugging

Windows:

```
set PWDEBUG=1 && yarn test

to unset debugging:
set PWDEBUG=
```

### Troubleshooting `firebase emulators:exec`

If `firebase emulators:exec` fails for unknown reason, try running `firebase emulators:exec "yarn test" || cat firebase-debug.log`.

### Tests that should be written

- Compile error, stdout, stderr
- Too large input
- Too large output
