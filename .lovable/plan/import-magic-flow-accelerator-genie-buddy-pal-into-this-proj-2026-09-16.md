# Import magic-flow-accelerator (Genie Buddy Pal) into this project

## What the source is

The GitHub repo is a complete Lovable-built app on the same TanStack Start stack as this project: an AI video studio with sign-in, a chat/brainstorm page, source video analysis, a channel page, a video editor ("studio"), and a scheduled-publish hook. It uses Lovable Cloud for login, database, and AI.

## What I'll do

1. **Copy the app code** from the downloaded repo into this project:
   - All pages: landing page, sign-in page, and the protected app section (home, chat, sources, channels, studio)
   - All components (video editor, analysis views, AI chat elements, full UI kit)
   - All library code (workspace hook, AI/analysis/studio/channel functions, scheduling, YouTube helpers)
   - Styles, config files, and package dependencies from its package.json
2. **Enable Lovable Cloud** for this project, then apply the database migration from the repo (profiles, projects, sources, source_videos, videos, posts, cron_config — all with row-level security and grants).
3. **Install dependencies** the imported code needs (AI SDK, streamdown, embla carousel, recharts, etc.).
4. **Verify**: build passes, sign-in flow works, and each page loads.

## Notes

- The repo's own login, database, and AI keys are not in the code (correctly) — enabling Lovable Cloud here provides fresh ones automatically, so the app works end-to-end without you supplying any secrets.
- Existing videos/projects from the original app are not in the repo, so this copy starts with a fresh, empty database.
- The URL you shared was the repo's settings page; I used the main repository instead. Lovable can't import GitHub repos directly, so I'm migrating the code manually.

## Technical details

- Source: https://github.com/bestmarket/magic-flow-accelerator (cloned read-only to /tmp/gh-import)
- Stack match: TanStack Start + Tailwind v4 + Supabase via Lovable Cloud — no framework conversion needed
- New env/secrets needed: none beyond what Lovable Cloud provisions
