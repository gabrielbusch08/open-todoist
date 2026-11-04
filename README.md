# open-todoist

A one-file redirect page, so a Notion page can open a project in the Todoist **app**. Notion only accepts web links, and Todoist's app links (`todoist://`) are not web links.

Link format: `https://gabrielbusch08.github.io/open-todoist/#<Todoist project ID>`, e.g. `#6ghQ34VjfcV5PX8J`. The page sends the browser to `todoist://project?id=<ID>`, which opens the Todoist app on that project. It also shows a button for the app and a link to the same project on the web.

The ID sits after the `#`, which browsers never send to a server. Served by GitHub Pages from `main`.

To let the page close its own tab in Firefox: `about:config` → `dom.allow_scripts_to_close_windows` → `true`.
