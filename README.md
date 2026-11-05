# Nice Dela Cruz: personal website

Live at **https://missniceph.github.io**

## What's here and how to update it

| File or folder | What it is | When you'd touch it |
|---|---|---|
| `index.html` | The words and links on your home page | To change any text, link or role |
| `_posts/` | **Your updates (articles).** One file per update | Every time you publish an update |
| `_drafts/TEMPLATE-copy-me.md` | A ready-made template for a new update. Never published | Copy it when starting an update |
| `images/updates/` | Photos for your updates | When an update has a photo |
| `images/headshot.jpg` | Your photo | To change your photo |
| `styles.css` | Colours, fonts and layout | To change colours (see below) |
| `_layouts/default.html` | The top menu and footer shared by every page | To change footer or menu links |
| `_layouts/post.html`, `_includes/`, `updates/` | How update pages and lists look | Rarely |
| `_config.yml` | Site name, description and settings | Rarely |
| `images/share.png` | The preview picture when someone shares your link | Rarely. Ask Claude to regenerate it if your title changes |
| `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` | The little "N" icon in browser tabs and on phone home screens | Never, unless you rebrand |
| `fonts/` | The two typefaces (Fraunces and Inter), stored with the site so it loads fast | Never |
| `404.html`, `robots.txt` | The "page not found" page, and a note for search engines | Never |

**The easy way to edit:** open a file on GitHub, click the pencil icon (✏️), make your change, then click **Commit changes**. The live site updates in about a minute. If you don't see the change, refresh the page, or open it in a private or incognito window.

## Publish an update

Updates appear on your home page (the 3 newest), on their own page at **missniceph.github.io/updates**, and in the top menu. The Updates section and menu link stay hidden until your first update is published.

**To publish:**

1. Open `_drafts/TEMPLATE-copy-me.md` on GitHub and copy all of its text. (Click the copy icon ⧉ above the file.)
2. Go to the `_posts` folder and click **Add file → Create new file**.
3. Name the file with the date, then a few words, ending in `.md`. For example:
   **`2026-11-20-training-lgus-in-cebu.md`**
   - The date in the name is the date shown on the update.
   - Use lowercase and dashes, no spaces.
4. Paste the template and replace the example text: the `title`, a one- or two-sentence `description`, and then your article below the second `---` line.
5. Click **Commit changes**. Your update is live in about a minute.

**Formatting** (the template shows all of these):

| To get | Type |
|---|---|
| A subheading | `## Subheading` on its own line |
| **Bold** | `**bold**` |
| *Italic* | `*italic*` |
| A link | `[words to click](https://example.com)` |
| A bullet list | Start each line with `- ` |
| A highlighted quote | Start the line with `> ` |
| A new paragraph | Leave an empty line |

**Photos:** upload the photo to `images/updates` first (**Add file → Upload files**). Keep it under about 300 KB; squoosh.app shrinks photos for free. Then:

- For a photo at the top, fill in `image:`, `image_alt:` (a short description for people who can't see the photo), and optionally `image_caption:` in the top part of the file. This photo is also used when the update is shared on Facebook or Messenger.
- For a photo inside the article, type `![short description](/images/updates/your-photo.jpg)` on its own line.

**Good to know:**

- **To fix a typo:** open the update in `_posts`, click the pencil ✏️, edit, and commit.
- **To unpublish an update:** delete the file from `_posts`, or move it into `_drafts`.
- **A date in the future** keeps the update hidden until that day. It only appears once GitHub next rebuilds the site, which happens whenever you change any file.
- **If something looks wrong** after you commit, GitHub usually couldn't read the top part of the file. Check that it starts and ends with `---`, and that the title and description are inside "straight quotes". GitHub emails you if a build fails.
- **Prefer to write in Word or Google Docs?** Send the text to Claude and ask for it to be posted as an update.

## Change your photo

1. Use a portrait or square photo, about 800 pixels wide and under about 200 KB. A phone photo is fine; you can shrink it for free at squoosh.app.
2. Name it exactly **`headshot.jpg`** (all lowercase).
3. On GitHub, open the `images` folder, click **Add file → Upload files**, drop it in, and commit. It replaces the old one.

If the photo is ever missing, the page shows a large "N" instead of a broken image.

## Edit text

Open `index.html` and search (Ctrl+F or Cmd+F) for the words you want to change. Each section starts with a big comment header like `<!-- ===== ABOUT ===== -->`. Change only the words *between* the tags:

```html
<h3>Chief of Staff</h3>
```

- **The line under your name:** search for `POSITIONING STATEMENT`. Three options are in the note just above it. Copy the one you want into the line that starts with `<p class="lede">`.
- **Dates for your roles:** each role has an empty `<p class="when"></p>`. Type a date inside, for example `<p class="when">2019 – 2022</p>`. Empty ones stay hidden.
- **Curly quotes and apostrophes:** the page uses ’ and “ ” rather than ' and ". Either works; the curly ones just look more polished.

## Your email

Search `index.html` for `data-user`. Your email is split at the **@**:

```html
data-user="delacruzcrystaleunice" data-domain="gmail.com"
```

The page puts it together only when someone uses the **Email me** button, so it never appears as text and is harder for spam bots to collect.

## Social media links

Search for `missniceph`. Your links are in two files: `index.html` (the hero and Nice to Know buttons and the Contact section icons) and `_layouts/default.html` (the footer at the bottom of every page). To change one, edit the address inside `href="..."` everywhere it appears. To remove an icon, delete its whole line, the one that starts with `<li>`.

## Change colours

At the top of `styles.css` is a list of colours. `--accent` is the terracotta used for buttons and highlights. The second list, a little further down, is for dark mode. If you change `--accent`, keep it dark enough for small text to stay readable. The current colour was chosen to pass accessibility contrast checks.

## Social share preview

When your link is pasted into Facebook, Messenger, Viber, LinkedIn or X, it shows `images/share.png` with your name and title. To check it, or to make Facebook refresh an old preview, paste your link into Facebook's Sharing Debugger: https://developers.facebook.com/tools/debug/
