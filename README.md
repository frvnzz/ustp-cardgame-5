# ✨ Welcome to Your Spark Template!
You've just launched your brand-new Spark Template Codespace — everything’s fired up and ready for you to explore, build, and create with Spark!

This template is your blank canvas. It comes with a minimal setup to help you get started quickly with Spark development.

🚀 What's Inside?
- A clean, minimal Spark environment
- Pre-configured for local development
- Ready to scale with your ideas
  
🧠 What Can You Do?

Right now, this is just a starting point — the perfect place to begin building and testing your Spark applications.

🧹 Just Exploring?
No problem! If you were just checking things out and don’t need to keep this code:

- Simply delete your Spark.
- Everything will be cleaned up — no traces left behind.

📄 License For Spark Template Resources 

The Spark Template files and resources from GitHub are licensed under the terms of the MIT license, Copyright GitHub, Inc.

## Note: Rollup optional native dependency issue

On some macOS/Node/npm setups, Rollup (used by Vite) may fail during `npm run build` with an error like:

```
Error: Cannot find module @rollup/rollup-darwin-arm64
```

Root cause: npm can sometimes skip installing optional, platform-specific native packages. The simplest fix is to remove `node_modules` and the lockfile and reinstall so npm re-resolves the optional dependency for your platform.

Commands that resolved the issue in this repo:

```bash
rm -rf node_modules package-lock.json
npm i
npm run build
```

If you prefer to avoid optional native modules, you can install without optionals:

```bash
npm i --no-optional
```

If problems persist, try clearing npm cache (`npm cache clean --force`) or using an npm/node LTS combo (Node 18/20) or `pnpm` which handles optional deps differently.

This note documents the local fix; if you hit this in CI, prefer `npm ci` with a lockfile that matches the registry.
