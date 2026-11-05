# Nice Dela Cruz: personal website

This is a one-page website. It uses three files:

- `index.html`: all the words on the page
- `styles.css`: colours, fonts and layout
- `images/`: your headshot goes here

To make a small change, open the file on GitHub, click the pencil icon (✏️), make your edit, and click **Commit changes**. The live site updates within a minute or two.

## Replace the headshot

1. Pick a photo. Portrait or square shapes work best. Keep it under about 500 KB so the page loads fast.
2. Rename it to exactly **`headshot.jpg`** (all lowercase).
3. On GitHub, open the `images` folder, click **Add file → Upload files**, drop in the photo, and commit.

The photo replaces the "N" placeholder automatically. If you only have a `.png`, either convert it to `.jpg` or open `index.html`, search for `images/headshot.jpg`, and change it to `images/headshot.png`.

## Edit text

Open `index.html` and search (Ctrl+F or Cmd+F) for the words you want to change. Each section has a big comment header like `<!-- ===== ABOUT ===== -->`, which makes it easy to find your place. Only change the words *between* the tags, for example:

```html
<h3>Chief of Staff</h3>
```

- **Positioning line:** near the top, look for `POSITIONING STATEMENT`. There are three options in the comment. Copy the one you like into the line just below it, the one that starts with `<p class="lede">`.
- **Adding dates to your experience:** each role has an empty `<p class="when"></p>`. Type a date inside it, for example `<p class="when">2019 – 2022</p>`. Empty ones stay hidden.

## Add your email

Search `index.html` for `YOUR-EMAIL-NAME`. Split your email at the **@**:

```html
data-user="nice" data-domain="example.com"
```

(That example is for `nice@example.com`.) The page puts the address together only when someone clicks **Email me**, so your email never appears on the page as plain text and is harder for spam bots to collect.

## Add your LinkedIn

Search `index.html` for `YOUR-LINKEDIN-URL` and replace the whole link with your profile address, for example `https://www.linkedin.com/in/your-name/`.

## Change colours

At the top of `styles.css` there's a list of colours. `--accent` is the terracotta used for buttons and highlights. The second list, a little further down, sets the dark-mode colours.
