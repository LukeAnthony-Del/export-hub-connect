# Export Hub + Export Connect

Two installable PWAs for consent-based private media transfer.

- **Export Connect:** https://lukeanthony-del.github.io/export-hub-connect/export-connect/
- **Export Hub:** https://lukeanthony-del.github.io/export-hub-connect/export-hub/

Export Connect lets a person explicitly select photos and videos to upload.
Export Hub is an administrator-only gallery with five-column media grids and
ZIP downloads. Supabase stores the private files. ntfy.sh carries only a
generic new-upload alert.

## One-time setup

1. Create a Supabase project.
2. Run `export-supabase.sql` in its SQL editor.
3. Enable anonymous sign-ins under Authentication → Providers.
4. Create the Hub email/password user under Authentication → Users.
5. Run the admin `update auth.users` statement shown at the top of
   `export-supabase.sql`, using that email.
6. Put the project URL and anon key in `export-config.js`.
7. Replace the ntfy topic in `export-config.js` with a long random value.

The profile photo is mandatory. Other media is selected through the device's
system picker; the web app cannot read or upload unselected library items.
