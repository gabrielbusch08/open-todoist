# open-todoist

A one-file redirect page, so a Notion page can open a project in the Todoist **app**. Notion only accepts web links, and Todoist's app links (`todoist://`) are not web links.

Link format: `https://gabrielbusch08.github.io/open-todoist/#<Todoist project ID>`, e.g. `#6ghQ34VjfcV5PX8J`. A whole Todoist project link pasted after the `#` works too. Notion's links carry `?v=3` so Firefox doesn't serve an old cached copy. The page sends the browser to `todoist://project?id=<ID>`, which opens the Todoist app on that project. It also shows a button for the app and a link to the same project on the web.

The ID sits after the `#`, which browsers never send to a server. Served by GitHub Pages from `main`.

The page closes its own tab only after the link "close this tab by itself from now on" was clicked once in that browser (kept in localStorage), because Firefox's first "Open Todoist?" question also takes the focus away.

Once that's on, the page is a blank dark tab (Notion's dark grey) that hands off after 0.1 s instead of 0.5 s; its text shows only if the app hasn't taken over after 2 s.
