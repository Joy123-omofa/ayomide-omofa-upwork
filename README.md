# Adeyanju J. — Book Editor (portfolio website)

A single-page, dependency-free portfolio site for a freelance book editor.
Navy · gold · white. Built to be hosted free on GitHub Pages.

**Live address:** `https://USERNAME.github.io` (once deployed)

---

## 1. The files

| File | Upload to the repo? | What it does |
|---|---|---|
| `index.html` | **Yes** | The entire site — HTML, CSS, JavaScript, structured data and the portrait photo, all in one file |
| `robots.txt` | **Yes** | Lets Google, Bing **and** AI answer engines (GPTBot, ClaudeBot, PerplexityBot…) crawl and cite the site |
| `sitemap.xml` | **Yes** | Submit this to Google Search Console to get indexed faster |
| `llms.txt` | **Yes** | A plain-text brief written for AI assistants, so they describe the services accurately |
| `README.md` | Optional | This file. GitHub shows it on the repo page; it never appears on the website |

There is no separate image file. The photo is embedded inside `index.html` as a
base64 data URI, so the site is genuinely one file and can never load with a
broken picture.

---

## 2. Put it on GitHub Pages (about 10 minutes, no terminal needed)

1. Create a GitHub account if you don't have one: <https://github.com/signup>
2. Click **+ → New repository**.
   - **Repository name:** `USERNAME.github.io` — replace `USERNAME` with your exact
     GitHub username. This exact name is what gives you the short address
     `https://USERNAME.github.io`.
   - Set it to **Public**. Click **Create repository**.
3. On the new repo page, click **uploading an existing file**.
4. Drag in the files from section 1.
5. Click **Commit changes**.
6. Go to **Settings → Pages**. Under *Build and deployment* set
   **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`**. Save.
7. Wait 1–3 minutes, then open **https://USERNAME.github.io** — the site is live.

> If you name the repo anything other than `USERNAME.github.io`, the address becomes
> `https://USERNAME.github.io/repo-name/` instead. Both work.

To change anything later: open the file on GitHub, click the pencil icon, edit,
commit. The live site updates within a minute or two.

---

## 3. Before you share the link — three jobs

### a) Replace the placeholder URL

Find and replace in all four files:

| Find | Replace with |
|---|---|
| `https://adeyanju-editorial.github.io/` | your real live address |
| `USERNAME` | your GitHub username |

The URL appears in `index.html` (meta tags and structured data), plus once or
twice in each of the three text files.

### b) Adding client reviews later

The **Client results** section no longer carries placeholder quote cards. It now shows the
verified record — Top Rated, 100% Job Success, 5.0 stars across 3 reviews, $2K+ earned — with a button
through to the Upwork profile where the reviews actually live. Nothing on the page claims a
quote that cannot be checked.

**To quote a review directly on the page, the words have to come from you.** Open your Upwork
profile, scroll to Work History, and copy a client's feedback exactly as written, along with their
name as Upwork displays it and the job title. Send that to me and I will set it; or do it yourself: paste the text into a
`<figure class="quote">` block inside a `<div class="quotes">` above the record panel. The `.quote`
styles are still in the stylesheet, ready to use.

**Do not invent reviews.** One verifiable review outperforms three impressive fake ones, and a
prospect who cross-checks a fabricated quote against your Upwork profile is a client you have
already lost.

### c) Check the twelve editorial examples

The **Proof** section shows twelve editing decisions, each as Original / Edit /
Margin comment. Examples **01–04** are yours, word for word. Examples **05–12**
were written to round out the range — dangling modifier, parallel structure,
agreement, redundancy, tense, rhythm, a developmental note that changes no wording,
and one where the "error" is deliberately left alone.

Read 05–12 as though you had written them, and rewrite anything that doesn't sound
like your margin voice. They are the single most persuasive thing on the page, so
they need to be yours.

### d) Optional — a social preview image

Create a 1200×630 image, name it `og-cover.png`, and upload it to the repo root.
It's what appears when someone shares the link on WhatsApp, LinkedIn or X. The
meta tags already point at it; until it exists, links share without a picture.

---

## 4. What's on the page

**Sections:** hero · services · process · proof · client results · about · FAQ ·
contact · closing call to action.

**Services** — five offerings (Manuscript Evaluation, Developmental Editing,
Line & Copy Editing, The Full Polish, Add-ons), all quoted per manuscript rather
than by rate card.

**Proof** — twelve editorial decisions in a tracked-changes window, filterable by
Copy edit · Line edit · Developmental · Voice preserved.

**FAQ** — 33 questions across five topics, filterable, with an accordion.

**Contact** — WhatsApp, email, Upwork, location and hours, plus a sample-edit
request form that composes a pre-written WhatsApp or email message from what the
visitor types. No backend, no database, nothing stored on the site — which is why
it works on GitHub Pages.

**Also built in:** sticky navigation with a scroll-progress bar and active-section
highlighting; a dark-navy / ivory theme switch that remembers the visitor's choice;
animated hero, aurora background, gold shimmer type, scroll reveals and count-up
statistics; a floating WhatsApp button and back-to-top control. Fully responsive,
keyboard accessible, honours `prefers-reduced-motion`, and has a print stylesheet.

### Contact details used throughout

- WhatsApp **+234 907 939 6845** → `https://wa.me/2349079396845`
- Email **joyomofaadeyanju71@gmail.com**
- Upwork `https://www.upwork.com/freelancers/~0135cdbe692513c067`

To change any of these, search `index.html` for `2349079396845`,
`joyomofaadeyanju71@gmail.com` or `0135cdbe692513c067` and replace every
occurrence, including the ones inside the `<script type="application/ld+json">`
block at the bottom.

---

## 5. The SEO / AEO / GEO / AIO layer

- **SEO** — title, meta description, keywords, canonical URL, Open Graph and
  Twitter cards, semantic heading hierarchy, descriptive link text, sitemap and
  robots file.
- **AEO (Answer Engine Optimisation)** — every major section opens with a bordered
  **answer block** stating the conclusion in one short paragraph, which is the
  format featured snippets and voice assistants extract. Backed by `FAQPage` and
  `HowTo` structured data.
- **GEO (Generative / Geographic Engine Optimisation)** — `geo.region`,
  `geo.position` and `ICBM` meta tags for Surulere, Lagos, plus `ProfessionalService`
  schema with a postal address, coordinates, opening hours and `areaServed` covering
  the US, UK, Canada, Australia and Nigeria. This is what lets you surface for both
  "book editor in Lagos" and "hire a nonfiction book editor".
- **AIO (AI Optimisation)** — `llms.txt`, an explicit AI-crawler allowlist in
  `robots.txt`, a `speakable` specification, and a JSON-LD `@graph` mirroring the
  whole page in machine-readable form so assistants quote your services, pricing
  policy and contact details correctly.

### After you go live

1. Add the site to **Google Search Console** (<https://search.google.com/search-console>)
   and submit `sitemap.xml`.
2. Add it to **Bing Webmaster Tools** — Bing feeds several AI answer engines.
3. Test the structured data at <https://search.google.com/test/rich-results>.
4. Put the link in your Upwork profile, your email signature and your social bios.
   Inbound links are still the strongest ranking signal there is.

---

## 6. Using a custom domain later

Buy a domain, then in **Settings → Pages → Custom domain** enter it and save.
GitHub creates a `CNAME` file for you. At your registrar, add four `A` records
pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and
`185.199.111.153`. Tick **Enforce HTTPS** once the option appears — it can take a
few hours. Then redo the URL replacement in section 3a.

---

© Adeyanju J. Editorial
