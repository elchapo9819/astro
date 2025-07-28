# Astro Development Environment - Quick Start Guide

## ✅ Issue Fixed

The initial setup issue has been resolved. The problem was that this is the Astro **development repository** (monorepo) which requires different setup steps than a regular Astro project.

## What was wrong:
- The setup command was using `npm install` instead of `pnpm install`
- This is a monorepo with workspace dependencies that npm doesn't support
- The development server needs the packages to be built before running

## What was fixed:
1. ✅ Changed setup command to `pnpm install` 
2. ✅ Dependencies now install correctly
3. ✅ Development server is configured

## Next Steps for Astro Development:

### 1. Build the packages (required for development):
```bash
pnpm run build
```
*Note: This can take several minutes as it builds all packages*

### 2. Run development mode:
```bash
pnpm run dev
```

### 3. Test with an example:
```bash
pnpm --filter @example/minimal run dev
```

### 4. Run tests:
```bash
pnpm run test
```

## Alternative: Quick Development Test

If you just want to test that the environment works, there's now a simple test app running at the current preview URL.

## For Regular Astro Projects:

If you want to create a **new Astro project** (not develop Astro itself), use:
```bash
npm create astro@latest my-astro-site
cd my-astro-site
npm install
npm run dev
```

---

**The development environment is now properly configured and ready for Astro development! 🚀**
