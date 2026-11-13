# Amber Finch website

Static website for Amber Finch, with a separate privacy policy for each app.
No build step, package installation, external fonts, analytics or JavaScript.

## Publish on GitHub Pages

1. Create a **public** repository named `amber-finch` under `sebvannistel`.
2. Upload the contents of this folder to its `main` branch, preserving directories.
3. Open repository **Settings → Pages**.
4. Choose **Deploy from a branch**, then **main** and **/ (root)**, and save.
5. Wait for deployment and open the URL GitHub provides. If GitHub offers Enforce HTTPS, enable it.

Expected URLs (not live until deployed):
- Home: https://sebvannistel.github.io/amber-finch/
- Sleep Timer policy: https://sebvannistel.github.io/amber-finch/sleep-timer/privacy/

After verifying the public policy page loads without login, set the live URL in
Sleep Timer's `publishing/policy/publisher.properties` and in Play Console.
Do not make the SleepTimer source repository public to host these files.

## Local preview

Run `python -m http.server 8080 --bind 127.0.0.1` in this folder and open
http://127.0.0.1:8080/ . Stop the server with Ctrl+C.

## Maintain

Keep the Sleep Timer policy synchronized with its app policy text. The website
adds a separate section about website hosting. Update the effective date when
practices change. Add future apps in their own directories, e.g.
`another-app/privacy/index.html`, and link them from the homepage.

The app is marked as preparing for release. Add the verified Google Play link
and update that label after it is publicly available. No Play listing is invented.
