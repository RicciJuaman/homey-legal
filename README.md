# homey-legal

The two pages Google Play requires to be reachable at a public URL, for the
Homey household app.

- **[delete-account.html](delete-account.html)** — how to delete your account.
  Play requires this of any app that lets people create an account, by two
  routes: one inside the app, and one on a web page that works without it
  installed. This is the second route.
- **[privacy.html](privacy.html)** — the privacy policy. Also a URL Play asks
  for, not a file.

## Why this repo exists separately

The app itself lives in a **private** repository. GitHub Pages will not build a
site from a private repo without a paid plan, and making the whole app public to
serve two static pages is a large change for a small reason. So the pages live
here, in a public repo of their own, and the app source stays private.

There is nothing else here on purpose: no build step, no dependencies, no
scripts. A page that needs compiling is a page that eventually stops being
published.

## Published at

<https://riccijuaman.github.io/homey-legal/>

GitHub Pages serves this repo's root on the `main` branch. Pushing to `main`
republishes within a minute or so.

## Keeping it honest

The wording of the privacy policy is mirrored from `docs/PRIVACY.md` in the
private `homey-home` repository, and the deletion page from
`docs/delete-account.html` there. **If you change one, change the other** — a
privacy policy that no longer matches what the code does is worse than none.

Two deliberate differences in `privacy.html`: the source file's "must be filled
in before publishing" list is a note to the developer rather than policy, so it
is not published, and its deletion-page placeholder resolves to a real link.

## Still to do

`privacy.html` carries a marked placeholder for the operator's legal name and
country of residence. It must be replaced with the real name before the app is
submitted to any store — a policy that does not say who is responsible for the
data is not a policy.
