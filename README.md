# International Model NATO (IMNATO) website

The public website for International Model NATO, published at **https://imnato.org**.

It is a plain, static website: ordinary HTML and CSS files, no database, no forms, and no tracking. It collects no information from visitors. GitHub Pages publishes it automatically: **any change saved to the `main` branch goes live within a minute or two.**

If you are new to this, read "Edit a page in your browser" below. You do not need to install anything.

## What is in this repository

| File or folder | What it is |
| --- | --- |
| `index.html` | Home page |
| `committees.html` | Committees |
| `schedule.html` | Schedule |
| `materials.html` | Materials |
| `register.html` | Registration information |
| `gallery.html` | Photo gallery |
| `contact.html` | Contact details |
| `css/style.css` | Colors, fonts, and layout for the whole site |
| `images/` | Logo, flags, and gallery photos |
| `files/` | Downloadable PDFs |
| `sitemap.xml`, `robots.txt` | Tell search engines which pages exist. **If you add or rename a page, add it to `sitemap.xml`.** |
| `favicon.ico` | The small icon shown in browser tabs and search results |
| `CNAME` | Tells GitHub the site lives at imnato.org. **Never delete or edit this file.** |

## Edit a page in your browser (no software needed)

1. On GitHub, open this repository and click the page file you want to change, for example `schedule.html`.
2. Click the pencil icon (**Edit this file**) at the top right of the file.
3. Change the words you want. Only edit the text between tags (the parts inside `< >`). Leave the tags themselves alone.
4. Click **Commit changes**, write a short note about what you changed (for example "Add 2027 fees"), and click **Commit changes** again.
5. Wait a minute or two, then reload imnato.org. Hold Shift while reloading if you do not see your change.

**Made a mistake?** Nothing is lost. Open the file, click **History**, find the last good version, and copy its text back in. Ask a more experienced student if you get stuck.

## Placeholders

Anything the conference still needs to fill in is marked like this: `[TODO: description]`. On the live site these show up **highlighted in yellow**. To find them all, use GitHub's search box (press `/`) and search for `TODO`.

**Do not announce the site as finished while any yellow text remains.**

## Common tasks

**Add a PDF** (for example the Delegation Handbook): open the `files` folder, click **Add file**, then **Upload files**, and commit. Then edit `materials.html` and link to it with `href="files/file-name.pdf"`.

**Add gallery photos:** upload them to `images/gallery/`, then follow the comment inside `gallery.html`. Add a short description of each photo (the `alt` text) for visitors who use screen readers. Only post photos you have the right to use.

**Add or remove a committee:** open `committees.html` and copy or delete one whole `<article>` ... `</article>` block.

**Update the Secretariat or Delegations (home page):** open `index.html` and find the section heading, "Secretariat 2027" or "Delegations". To change a person or a university, edit the text. The Secretariat is shown in four centered rows from most senior at the top; each `<ul>` is one row, and to add a person you copy one whole `<li>` ... `</li>` block into the row where they belong. A country with no university yet shows only its name; to assign one, type the university name after the `<br>` under the country name.

**Change colors or fonts:** edit the values at the top of `css/style.css`, in the section called `:root`.

**Change the menu, banner, or footer:** these are repeated on all seven pages. Make the same change in every `.html` file, or the pages will not match.

## Updating for a new conference year

- [ ] Update the edition number, dates, and venue on every page (search for the old year)
- [ ] Update the banner at the top of every page, and the footer year
- [ ] Update the event data on the home page, the sitemap dates, and the preview image (see "Search visibility" above)
- [ ] Update fees, deadlines, schedule, committees, Secretariat, delegations, and contacts
- [ ] Replace the materials in `files/` and the photos in `images/gallery/`
- [ ] Check that the flag strip on the home page still matches the current list of NATO member states
- [ ] Search for `TODO` and clear every placeholder
- [ ] Check the domain renewal (see the Handover Guide)

## Search visibility (SEO)

Each page has a title, a description, and a "canonical" address, and the home page also carries **event data** that tells Google the conference's name, dates, and location.

When the conference details change each year:
- Update the dates, name, and location in the event data on `index.html` (search the file for `application/ld+json`).
- Update the page titles and descriptions at the top of each page file if they mention the year, edition, or dates.
- Update the `lastmod` dates in `sitemap.xml`.
- In Google Search Console, check that the site is still verified and request indexing of the home page after big changes.

When someone shares a link to the site, the preview picture comes from `images/social-preview.png`. Replace that image if the dates or branding change.

## Rules for this repository

This repository is **public**, so anyone on the internet can read every file in it, including old versions.

- Never add passwords, private documents, or personal information about students.
- Do not delete `CNAME`.
- Keep this README accurate. If you change how the site works, update it.

## Credits

- Country flags: [flag-icons](https://github.com/lipis/flag-icons), MIT license (see `images/flags/LICENSE-flag-icons.txt`).
- The NATO/OTAN emblem is used with permission of the conference organizers. The current image is a small crop from the old website and looks soft at large sizes. Replace `images/nato-emblem.png` with a higher-resolution version when one is available.

## Who to ask

The Handover Guide (kept separately by the site owner) lists the accounts, the domain, who has access, and the yearly maintenance tasks. Ask the current owner for access to it.
