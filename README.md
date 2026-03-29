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

## Deploy to Netlify (FREE — ~5 minutes)

1. Go to **netlify.com** and create a free account
2. From the dashboard, find the **"Deploy manually"** section
3. Drag and drop the entire **flionlion** folder onto the deploy area
4. Netlify gives you a live URL immediately (e.g. `random-name.netlify.app`)
5. Go to **Domain settings** → Add custom domain → enter `flionlion.com`
6. Update your domain registrar's nameservers to point to Netlify (they give you exact instructions)

That's it. Total cost: $0 for hosting. You only pay for your domain (~$12/year).

---

## Activate the Contact Form

The contact form on contact.html uses Formspree (free tier):

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
