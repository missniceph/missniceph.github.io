# Nice Dela Cruz: personal website

Live at **https://missniceph.github.io**

## What's here and how to update it

| File or folder | What it is | When you'd touch it |
|---|---|---|
| `index.html` | All the words and links on the page | To change any text, link or role |
| `styles.css` | Colours, fonts and layout | To change colours (see below) |
| `images/headshot.jpg` | Your photo | To change your photo |
| `images/share.png` | The preview picture that shows when someone shares your link | Rarely. Ask Claude to regenerate it if your title changes |
| `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` | The little "N" icon in browser tabs and on phone home screens | Never, unless you rebrand |
| `fonts/` | The two typefaces (Fraunces and Inter), stored with the site so it loads fast | Never |
| `404.html` | The "page not found" page | Never |
| `.nojekyll` | Tells GitHub to publish the files exactly as they are | Never. Don't delete it |

**The easy way to edit:** open a file on GitHub, click the pencil icon (✏️), make your change, then click **Commit changes**. The live site updates in about a minute. If you don't see the change, refresh the page, or open it in a private or incognito window.

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

Search `index.html` for `missniceph`. Your links appear in **three** places: the hero and Nice to Know buttons (Instagram), the Contact section icons, and the footer. To change one, edit the address inside `href="..."` everywhere it appears. To remove an icon, delete its whole line, the one that starts with `<li>`.

## Change colours

At the top of `styles.css` is a list of colours. `--accent` is the terracotta used for buttons and highlights. The second list, a little further down, is for dark mode. If you change `--accent`, keep it dark enough for small text to stay readable. The current colour was chosen to pass accessibility contrast checks.

## Social share preview

When your link is pasted into Facebook, Messenger, Viber, LinkedIn or X, it shows `images/share.png` with your name and title. To check it, or to make Facebook refresh an old preview, paste your link into Facebook's Sharing Debugger: https://developers.facebook.com/tools/debug/
