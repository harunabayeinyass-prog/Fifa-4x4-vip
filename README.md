# FIFA 4x4 VIP AI — testing website

## Files
- `index.html`: website interface
- `style.css`: design
- `app.js`: Supabase authentication and odds-implied probability calculation
- `_headers`: basic Cloudflare Pages security headers

## Connect Supabase
1. In Supabase, open Project Settings → API.
2. Copy the Project URL and the publishable key (or legacy anon key).
3. Open `app.js` and replace `SUPABASE_URL` and `SUPABASE_ANON_KEY`.
4. Never use the `service_role` key or a secret key in browser code.
5. Commit and push the updated file to GitHub.

New signups are created as pending VIP profiles by the database trigger. Your administrator must approve members through a trusted admin-only process. Do not expose admin credentials or add a public profile-update policy.

## Cloudflare Pages
Connect the GitHub repository to Cloudflare Pages. Use the repository root as the build directory. No build command is needed; output directory is `/`.

## Important limitations
This is a testing starter, not a completed production AI product. It currently displays normalized bookmaker-implied probabilities. It does not yet include secure in-app admin approval, cloud match-history management, a trained prediction model, or an external licensed match-data feed. Complete and test those components before accepting paid VIP members.
