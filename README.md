It should be possible to render Grist documents on static sites
without any special back end. This is a playground for that.
Nothing that works here yet.

 * Need a data engine that is browser-friendly.
   There's a Pyodide flavor that should be usable with some tweaks.
   https://github.com/gristlabs/grist-core/pull/437
 * Need a pure javascript library for interacting with Sqlite.
   There's plenty of them now.
 * Need to fiddle with bundling to pull out enough of the "server"
   code and disentangle any dependencies that won't work in browser.

Getting Pyodide in upstream will help keep this clean.
Another step is making the Sqlite libraries pluggable.
I've revived an old better-sqlite3 fork as a starting
point for that, because it has some useful fixes,
even though it doesn't matter for the static file project.
