# flionlion.com — Complete Site

Jordan Quellman · Director + DP  
Wizard of Oz Technicolor palette × Paper Moon (Futura/Josefin Sans) typography

---

## Files

```
index.html          ← Home page (hero, work list, about strip, contact CTA)
films.html          ← Fictional films (features + shorts grid)
documentary.html    ← Documentaries (featured + full grid)
commercial.html     ← Commercials, music videos, editorial
photography.html    ← Photo grids (documentary stills, on set, portraits)
about.html          ← Full bio, stats, awards, press quotes
contact.html        ← Contact info + inquiry form
style.css           ← All shared styles
main.js             ← All shared JavaScript (grain, cursor, HUD, reveal)
```

---

## Deploy to GitHub Pages (FREE — ~5 minutes)

1. Go to **github.com** and create a free account (if you don't have one)
2. Click **"New repository"** — name it `flionlion` (or anything you like)
3. Set it to **Public**, then click **"Create repository"**
4. Upload your files:
   - Click **"uploading an existing file"** on the repo page
   - Drag and drop all the files from this folder (not the folder itself — the files inside)
   - Click **"Commit changes"**
5. Go to **Settings → Pages** (in the left sidebar)
6. Under **"Source"**, select **"Deploy from a branch"**
7. Choose branch: `main`, folder: `/ (root)` → click **Save**
8. GitHub gives you a live URL: `https://yourusername.github.io/flionlion`

### Using a Custom Domain (flionlion.com)

1. In **Settings → Pages**, enter `flionlion.com` in the **"Custom domain"** field and save
2. GitHub will create a `CNAME` file in your repo automatically
3. Go to your domain registrar and add these DNS records:

   **Option A — Apex domain (flionlion.com):**
   Add 4 A records pointing to GitHub's IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

   **Option B — www subdomain (www.flionlion.com):**
   Add a CNAME record:
   ```
   www → yourusername.github.io
   ```

4. DNS changes take up to 24 hours to propagate
5. Once live, check **"Enforce HTTPS"** in Settings → Pages for a free SSL certificate

Total cost: $0 for hosting. You only pay for your domain (~$12/year).

---

## Activate the Contact Form

The contact form on contact.html uses Formspree (free tier) — this works on GitHub Pages:

1. Go to **formspree.io** and sign up free
2. Create a new form — you get a unique form ID
3. Open `contact.html`, find this line:
   ```
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
4. Replace `YOUR_FORM_ID` with your actual ID
5. Form submissions go straight to your email

---

## Adding Your Real Videos

Currently all video cards show placeholder color backgrounds.  
To add real video thumbnails, replace the `.vid-card-bg` background with an image:

```css
.vid-card-bg {
  background-image: url('your-thumbnail.jpg');
  background-size: cover;
  background-position: center;
}
```

Or add an `<img>` tag inside each `.vid-card`:
```html
<img src="thumbnails/typical.jpg" alt="Typical" 
     style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;opacity:0.6;">
```

To link cards to Vimeo/YouTube, wrap them in `<a href="https://vimeo.com/...">`.

---

## Customizing Content

All content is plain HTML — just find and replace text directly in each file.  
The color system uses CSS variables in `style.css`:

| Variable | Color | Used for |
|----------|-------|----------|
| `--ruby` | Red | Narrative, featured |
| `--yellow` | Gold | Yellow Brick Road accent |
| `--emerald-l` | Green | Documentary, nature |
| `--sky` | Blue | Editorial, sky |
| `--violet-l` | Purple | Music, Glinda |
| `--poppy` | Orange | Poppy field accent |

---

## Pages to Add Later

- `music.html` — Music videos standalone page
- `episodic.html` — Episodic work
- `branded.html` — Branded content
- `fashion.html` — Fashion work

These are linked from the home page work list but not yet created.  
They follow the exact same pattern as `films.html` — just duplicate and edit.
