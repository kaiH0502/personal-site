# Personal site

Plain HTML + one CSS file. No build step, no dependencies, no framework.
Open any `.html` in a browser and it works.

```
index.html                    home — name, tagline, hero image, top articles
about/index.html              about page
articles/index.html           article index, grouped by year
articles/hello-world/         one article (copy this folder to add a new one)
gallery/index.html            photo grid
assets/style.css              all styling — every color/size lives at the top
assets/placeholder.svg        stand-in image, replace with your photos
```

## Preview locally

```bash
python3 -m http.server 4321
```

Then open http://localhost:4321

## Make it yours

1. Replace `Kai Huang` and the tagline in all five HTML files.
2. Swap the footer links (Instagram / X / LinkedIn / Email) for your real ones.
3. Drop your photos into `assets/` and point the `<img src>` at them.
4. Tune the look from the `:root` block at the top of `assets/style.css` —
   `--column` controls the text width, `--serif` the display font.

## Add an article

```bash
cp -r articles/hello-world articles/my-new-post
```

Edit the title, date and body inside it, then add an `.entry` block linking
to `/articles/my-new-post/` in `articles/index.html`.

## Deploy (free)

**Netlify Drop** — go to https://app.netlify.com/drop and drag this folder in.
Live in about ten seconds. Easiest option.

**Vercel or Cloudflare Pages** — push the folder to a GitHub repo, import it,
choose "no framework / static". Every push redeploys.

**GitHub Pages** — push to a repo, then Settings → Pages → deploy from branch.

## Custom domain

Buy a domain (Namecheap, Cloudflare, Porkbun — ~$10–15/yr), then add it under
your host's domain settings and follow their DNS instructions. HTTPS is
automatic on all three hosts above.
