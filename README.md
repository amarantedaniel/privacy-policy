# App pages

I keep the privacy policies and support pages for my apps here. I give each app its own directory with `privacy.html` and `support.html`. My home page lists all apps, and I use `assets/style.css` to keep their layouts consistent.

## Published URLs

I publish the repository root from the `main` branch through GitHub Pages. My repository is `amarantedaniel/app-pages`, with the base URL `https://amarantedaniel.com/app-pages/`.

| App | Privacy policy path | Support path |
| --- | --- | --- |
| Pawfect Name | `pawfect-name/privacy.html` | `pawfect-name/support.html` |
| Forgetful | `forgetful/privacy.html` | `forgetful/support.html` |
| Sverigekliv | `sverigekliv/privacy.html` | `sverigekliv/support.html` |
| Take Your Creatine | `take-your-creatine/privacy.html` | `take-your-creatine/support.html` |

I append each path to the published base URL when setting links in App Store Connect and inside my apps. I update those links after a repository rename because GitHub Pages does not redirect the former URLs.

## Editing pages

I edit each app's HTML directly. I keep policy and support content specific to the app, and I update a policy's date when its meaning changes. For Sverigekliv, I maintain Swedish and English sections with language navigation.

When I add an app, I create a directory named after its public name, add both pages using an existing page's document structure and navigation, and add links to `index.html` and the table above. I use `../assets/style.css` and the mobile viewport meta tag on every app page.

## Local preview

I run `mise install`, then `mise exec -- python -m http.server 8000`, and open `http://localhost:8000/`. I use Python only for local preview; publishing requires no build step.
