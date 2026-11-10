# EduSphere 360

Online-first education management platform built with React, TypeScript, Vite and Supabase.

## Current release source
This repository contains the current workspace update prepared on 10 November 2026. See `PREMIUM_WORKSPACE_UPDATE_REPORT.md` for implemented changes, verification results and release limitations.

## Development
- `npm ci`
- `npm run verify:project`
- `npm run test:user-errors`
- `npm run test:finance`
- `npm run test:file-access`
- `npm run test:campus`
- `npm run build`

Set `VITE_SUPABASE_URL` and `VITE_SUPABASE_PUBLISHABLE_KEY` in the build environment. Never expose a Supabase service-role key in the browser.

## Production release
The GitHub Actions workflow verifies and builds the project on pushes and pull requests. Cloudflare production deployment remains a manual workflow dispatch requiring the configured Cloudflare credentials and production environment approval.

The source package is not itself a Cloudflare Pages upload bundle. Deploy only the generated `dist/` output after a successful build.
