# baton-smoketest

Throwaway target repo for smoke-testing [Baton](https://github.com/tooaverage)'s
"share with eng" flow. Baton pushes branches and opens real PRs against this
repo so the flow can be exercised without polluting a real client project.

**This is not real work.** Anything merged, opened, or committed here is
disposable. Feel free to nuke branches, close PRs, or delete the repo entirely
at any time.

## What's in here

A single `index.html` — a boring static page with a headline, some lorem
ipsum, and a pink button. Just enough to screenshot and to have something
visible when a Baton-generated PR lands.

## Running locally

```sh
cd ~/dev/baton-smoketest
python3 -m http.server 5173
```

Then open <http://localhost:5173/>.

## Testing Baton against this repo

Before each test run, branch off `main` so Baton's "not on main" preflight
check doesn't block you:

```sh
git checkout main
git pull
git checkout -b feature/<something>
```
