# MX Bikes Records — Online Edition

This folder contains the current MX Bikes Records interface plus the database/authentication setup needed to turn it into a shared online app.

## Recommended stack
- Frontend: the included `index.html`
- Database + authentication: Supabase
- Hosting: Vercel, Netlify, or another static host

## Database model
Use these tables:
- `profiles`: user/player profiles and admin role
- `tracks`: track names
- `bikes`: bike manufacturer/model
- `laps`: player, track, bike, lap time, date, note, created/updated timestamps

## Important behavior
Overall and bike-specific records should be calculated from the lap table rather than stored as separate mutable records. This means editing/deleting a lap automatically changes the leaderboard and record holder.

## Before deployment
1. Create a Supabase project.
2. Run `supabase_schema.sql` in Supabase SQL Editor.
3. Enable email/password authentication.
4. Put the Supabase project URL and anon key into the frontend configuration.
5. Deploy this folder to Vercel/Netlify.

The current HTML remains usable locally with its existing browser storage until the cloud connection is configured.
