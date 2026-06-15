# Ava's List

A private shared list for tracking pregnancy prep — shopping, to-dos, and questions
for the doctor. One self-contained `index.html`, backed by Supabase. Two phones,
one shared list, live within a few seconds.

## How it works
- The whole app is `index.html` — no build step, no framework, no CDN. Edit it in
  any text editor, commit, and push; GitHub Pages redeploys automatically.
- Data lives in one Supabase row (`shared_lists`, id `avas-main`) as a JSON blob.
- No login. Anyone with the page URL can view and edit. Keep the link private.

## If saving ever breaks (HTTP 521 / "offline")
The Supabase free tier **pauses the project after ~1 week of inactivity**, which
stops it resolving and breaks saving. If that happens, open the Supabase dashboard
and **Resume** the project — data is preserved. Then it works again.

## Editing
Change `index.html`, then:
```
git add index.html && git commit -m "tweak" && git push
```
Pages updates within a minute or two.
