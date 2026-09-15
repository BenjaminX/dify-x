---
name: new-slide-deck
description: Create a new reveal.js slide deck for dify-x and register it on the index pages. Use when asked to add a new presentation, create a new deck, or add slides for a new customer/event.
---

# New Slide Deck

Creates a new reveal.js presentation in `/Users/banana/Work/dify-x/` and wires it into the navigation index.

The repository currently holds 15 decks. Always re-read the directory listing before writing — new decks land frequently and the inventory in `README.md` may lag by a commit or two.

---

## Step 1 — Gather info

Ask (or infer from context) before writing any files:

| Field | Example |
|---|---|
| `DECK_DIR` | `acme` (lowercase, kebab-case) |
| `PILL_LABEL` | `Dify × Acme` |
| `THEME` | `editorial` · `nordic` · `milvus` · `popart` _(see §Themes)_ |
| ZH title + one-line description | for `index_zh.html` card |
| EN title + one-line description | for `index_en.html` card |
| Slide content outline | titles, bullets, speaker notes per slide |

Default to a **bilingual** deck: `index.html` (zh-CN) + `index_en.html` (en) that share slide order, `data-slide-id`s, timing, and speaker notes.

---

## Step 2 — Choose a theme

### Theme A · Editorial (default) — `enterprise-agent-campus` / `stripe-agent-workshop`

Newest and most polished. Reference-page aesthetic: 3px Dify Blue top rule, white top bar, hairline rules, single-column editorial grid. Best for lectures, workshops, and product-form talks.

- **CSS**: copy `../enterprise-agent-campus/editorial.css` as your base, plus `../enterprise-agent-campus/editorial-zh.css` for the Chinese page only
- **Reveal version**: `4.5.0`, vendored at `../agent-plugin-governance/assets/reveal/` (`reset.css`, `reveal.css`, `reveal.js`, `plugin/notes/notes.js`)
- **Fonts**: Inter + Noto Sans SC + JetBrains Mono (Google Fonts)
- **Canvas**: 1920 × 1080, `margin: 0.04`
- **Structure**: `<div class="deck-brand">` for the top bar, `<div class="lang-switch">` for CN/EN, then `<div class="reveal"><div class="slides">`
- **Classes**: `.cover-slide` / `.photo-bg` / `.cover-shade` / `.cover-copy` / `.cover-meta`, `.eyebrow`, `[data-slide-id]` on every section
- **Cache-busting**: version the CSS links (`editorial.css?v=YYYYMMDD-n`)
- **Also ship**: `README.md`, `source-map.md`, and `qa/contact-sheet-{zh,en}.png`

### Theme B · Nordic — `agent-systems` / `hongkong-oss` / `pupu` / `agent-last-mile`

Clean, grid-based, Dify Blue on white. Best for technical deep-dives.

- **CSS**: reference `../agent-systems/styles.css`
- **Reveal version**: `4.5.0` from CDN
- **Fonts**: Inter + Noto Sans SC + JetBrains Mono (Google Fonts)
- **Icons**: RemixIcon `remixicon@3.5.0`
- **Extra**: Tailwind CDN for utility classes
- **`<html lang>`**: `zh-CN` / `en`
- **Default bg**: `data-background-color="#fafafa"` (light) or `"#0033ff"` (brand)
- **Cover layout**: `.slide-hero` with `.author-block` (name / role / email)

### Theme C · Milvus — `milvus`

Three switchable sub-themes (Swiss / Atelier / Ukiyo) via keyboard `1` / `2` / `3`.

- **CSS**: `../milvus/styles/dify-theme.css` + `../milvus/styles/base.css` + `../milvus/styles/theme-swiss.css` (default)
- **Reveal version**: `5`
- **Fonts**: Söhne (fallback: Inter) + Noto Sans SC
- **`width × height`**: `1920 × 1080`
- **Classes available**: `.grid-2`, `.callout`, `.pill`, `.scribble`, `.emph`, `mark`, `.hl`, `.centered`, `section.card`, `section.accent`
- **Sub-themes**:
  - `theme-swiss.css` — minimal, white bg, subtle blue diffusion
  - `theme-atelier.css` — richer gradient, warmer, expressive
  - `theme-ukiyo.css` — washi paper texture, indigo brush underline on h2

### Theme D · Pop Art — `aispeech`

Bold, comic-strip aesthetics. Best for high-energy keynote-style talks.

- **CSS**: `../aispeech/styles/nordic.css` + `../aispeech/styles/popart.css`
- **Reveal version**: `4.5.0`
- **Palette**: `--pop-yellow #FFE900`, `--pop-red #FF3333`, `--pop-cyan #00FFFF`, `--pop-blue #3366FF`
- **Hard shadows**: `8px 8px 0 #000` — zero border-radius
- **Icons**: Font Awesome `@6.5.2`

### Bundled runtime

`agent-plugin-governance/assets/reveal/` holds a vendored reveal.js **4.5.0**. Reuse it via `../agent-plugin-governance/assets/reveal/...` rather than adding another copy. Only `ctrip/`, `dentsply/`, `paypal/`, and `milvus/` use CDN 5.x; everything else uses 4.5.0.

---

## Step 3 — Create the deck files

### Editorial skeleton (default)

```html
<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>{ZH_TITLE} — {PILL_LABEL}</title>
  <link rel="icon" href="../assets/logo.svg" type="image/svg+xml">
  <link rel="stylesheet" href="../agent-plugin-governance/assets/reveal/reset.css">
  <link rel="stylesheet" href="../agent-plugin-governance/assets/reveal/reveal.css">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Noto+Sans+SC:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="../enterprise-agent-campus/editorial.css?v=1">
  <link rel="stylesheet" href="../enterprise-agent-campus/editorial-zh.css?v=1">
</head>
<body>
  <div class="deck-brand"><img src="../assets/logo.svg" alt="Dify"><span>{PILL_LABEL} · {SHORT_TITLE}</span></div>
  <div class="lang-switch"><a class="active" href="index.html">中文</a><span>/</span><a href="index_en.html">EN</a></div>

  <div class="reveal"><div class="slides">

    <!-- 01 · VISUAL_SLOT: cover -->
    <section class="cover-slide" data-slide-id="s01-cover">
      <div class="cover-copy">
        <div>
          <div class="eyebrow on-dark">{PILL_LABEL}</div>
          <h1>{ZH_TITLE}</h1>
          <p>{ZH_SUBTITLE}</p>
        </div>
        <div class="cover-meta">
          <span>crazywoola（Banana） · Head of DevRel · Dify</span>
          <b>45 MIN</b>
        </div>
      </div>
      <aside class="notes">Speaker notes here.</aside>
    </section>

    <!-- 02 -->
    <section data-slide-id="s02-section">
      <div class="eyebrow">Section · Label</div>
      <h2>Slide headline that carries the conclusion.</h2>
      <aside class="notes">Speaker notes here.</aside>
    </section>

    <!-- Add more slides ══ -->

  </div></div>

  <script src="../agent-plugin-governance/assets/reveal/reveal.js"></script>
  <script src="../agent-plugin-governance/assets/reveal/plugin/notes/notes.js"></script>
  <script>
    Reveal.initialize({
      hash: true,
      width: 1920,
      height: 1080,
      margin: 0.04,
      transition: 'fade',
      backgroundTransition: 'fade',
      plugins: [RevealNotes],
    });
  </script>
</body>
</html>
```

For `index_en.html`: `lang="en"`, drop `editorial-zh.css`, swap `editorial.css` for the English variant if the deck ships one (see `stripe-agent-workshop/editorial-en.css`), and flip the `.lang-switch` active class. Keep `data-slide-id`s identical between languages.

### Nordic skeleton

```html
<!doctype html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>{ZH_TITLE} — Dify</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reset.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reveal.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/theme/white.css" id="theme">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/plugin/highlight/github.css">
    <link href="https://cdn.jsdelivr.net/npm/remixicon@3.5.0/fonts/remixicon.css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Noto+Sans+SC:wght@400;500;700&family=JetBrains+Mono&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="../agent-systems/styles.css">
</head>
<body>
    <div class="lang-switch">
        <a class="active" href="index.html">中文</a>
        <span>/</span>
        <a href="index_en.html">EN</a>
    </div>
    <div class="nordic-logo">
        <img src="../assets/logo.svg" alt="Dify" class="nordic-logo-img">
        <span class="nordic-logo-text">{SHORT_LABEL}</span>
    </div>
    <div class="reveal">
        <div class="slides">

            <!-- ══ Slide 1 · Cover ══ -->
            <section data-background-color="#fafafa">
                <div class="slide-hero text-center" style="max-width:860px;">
                    <h1 style="font-size:2.8rem;line-height:1.1;">{ZH_TITLE}</h1>
                    <p class="slide-subtitle" style="margin:1.2rem auto 0;max-width:560px;">{ZH_SUBTITLE}</p>
                    <div style="width:48px;height:3px;background:var(--dify-blue);border-radius:2px;margin:2rem 0 1.5rem;"></div>
                    <div class="author-block" style="align-items:center;margin-top:0;">
                        <div class="author-name">crazywoola（Banana）</div>
                        <div class="author-meta">Developer Relations @ Dify</div>
                        <div class="author-email">banana@dify.ai</div>
                    </div>
                </div>
                <aside class="notes">Speaker notes here.</aside>
            </section>

            <!-- ══ Add more slides ══ -->

        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reveal.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/plugin/notes/notes.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/plugin/highlight/highlight.js"></script>
    <script>
        Reveal.initialize({
            hash: true,
            transition: 'fade',
            backgroundTransition: 'fade',
            plugins: [RevealNotes, RevealHighlight],
        });
    </script>
</body>
</html>
```

### Milvus skeleton (with theme switcher)

```html
<!doctype html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>{ZH_TITLE} — Dify</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@5/dist/reveal.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@5/dist/theme/white.css" id="reveal-theme">
    <link rel="stylesheet" href="../milvus/styles/dify-theme.css">
    <link rel="stylesheet" href="../milvus/styles/base.css">
    <link rel="stylesheet" id="theme-variant" href="../milvus/styles/theme-swiss.css">
</head>
<body>
    <div class="lang-switch">
        <a class="active" href="index.html">中文</a>
        <span>/</span>
        <a href="index_en.html">EN</a>
    </div>
    <div class="brand"><img src="../assets/logo.svg" alt="Dify"></div>
    <div class="reveal">
        <div class="slides">
            <!-- ══ Slide 1 · Cover ══ -->
            <section>
                <h1 class="title-big">{ZH_TITLE}</h1>
                <p class="subtitle">{ZH_SUBTITLE}</p>
                <p class="meta">crazywoola（Banana） · Developer Relations @ Dify · banana@dify.ai</p>
                <aside class="notes">Speaker notes here.</aside>
            </section>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@5/dist/reveal.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@5/plugin/notes/notes.js"></script>
    <script>
        Reveal.initialize({ hash: true, width: 1920, height: 1080, margin: 0.04, slideNumber: 'c/t', transition: 'fade', plugins: [RevealNotes] });
        const themeLink = document.getElementById('theme-variant');
        const setTheme = (n) => { themeLink.href = `../milvus/styles/${n}.css`; };
        window.addEventListener('keydown', (e) => {
            if (e.key === '1') setTheme('theme-swiss');
            if (e.key === '2') setTheme('theme-atelier');
            if (e.key === '3') setTheme('theme-ukiyo');
        });
    </script>
</body>
</html>
```

### Pop Art skeleton

```html
<!doctype html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <title>{ZH_TITLE} — Dify</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reset.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reveal.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/theme/white.css" id="theme">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/plugin/highlight/monokai.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.5.2/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="../aispeech/styles/nordic.css">
    <link rel="stylesheet" href="../aispeech/styles/popart.css">
</head>
<body>
    <div class="lang-switch">
        <a class="active" href="index.html">中文</a>
        <span>/</span>
        <a href="index_en.html">EN</a>
    </div>
    <div class="reveal">
        <div class="slides">
            <section data-background-color="#FFE900">
                <div style="border:3px solid #000;padding:48px;box-shadow:12px 12px 0 #000;max-width:900px;">
                    <div style="font-size:1rem;font-weight:900;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:16px;">{PILL_LABEL}</div>
                    <h1 style="font-size:3.2rem;font-weight:900;line-height:1.05;color:#000;">{ZH_TITLE}</h1>
                    <p style="font-size:1.3rem;margin-top:24px;color:#000;">{ZH_SUBTITLE}</p>
                    <div style="margin-top:32px;font-size:0.9rem;font-weight:700;">crazywoola（Banana） · Developer Relations @ Dify</div>
                </div>
                <aside class="notes">Speaker notes here.</aside>
            </section>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reveal.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/plugin/notes/notes.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/plugin/highlight/highlight.js"></script>
    <script>
        Reveal.initialize({ hash: true, transition: 'none', backgroundTransition: 'none', plugins: [RevealNotes, RevealHighlight] });
    </script>
</body>
</html>
```

---

## Step 4 — Common slide patterns

### Two-column grid (Nordic / Milvus)
```html
<section>
    <h2>Section Title</h2>
    <div class="grid-2" style="margin-top:1.5rem;">
        <div class="callout"><strong>Left point</strong><br>Detail text here.</div>
        <div class="callout"><strong>Right point</strong><br>Detail text here.</div>
    </div>
</section>
```

### Pill + numbered list (Nordic)
```html
<section data-background-color="#fafafa">
    <div class="slide-label">
        <span class="pill">Section Name</span>
    </div>
    <h2 class="slide-title">Slide Title</h2>
    <div class="step-list">
        <div class="step-item"><span class="step-num">01</span><div class="step-content"><strong>Point</strong><p>Description</p></div></div>
        <div class="step-item"><span class="step-num">02</span><div class="step-content"><strong>Point</strong><p>Description</p></div></div>
    </div>
</section>
```

### Dark brand slide (Nordic)
```html
<section data-background-color="#0033ff">
    <div class="slide-hero text-center">
        <h2 style="color:#fff;font-size:2.2rem;">Key Message</h2>
        <p style="color:rgba(255,255,255,0.85);">Supporting detail</p>
    </div>
</section>
```

### Closing slide (Milvus style)
```html
<section>
    <div class="centered">
        <img src="../assets/logo.svg" class="logo-large" alt="Dify">
        <h2>{ZH_CLOSING_HEADLINE}</h2>
        <p class="meta">banana@dify.ai</p>
    </div>
</section>
```

### Vertical stack (nested sections)
```html
<section>
    <section><!-- horizontal parent --></section>
    <section><!-- vertical child 1 --></section>
    <section><!-- vertical child 2 --></section>
</section>
```

---

## Step 5 — Register on index pages

The index is **not** a card grid. Both `index_zh.html` and `index_en.html` use a two-pane editorial layout: a fixed hero on the left and a scrollable `<section class="deck-list">` of `.deck-row` entries on the right.

Append a new row as the **last** child of `<section class="deck-list">`, then renumber every `row-num` so the sequence stays contiguous from `00`:

```html
        <a class="deck-row" href="{DECK_DIR}/index.html">
          <span class="row-num">{NN}</span>
          <div class="row-body">
            <div class="row-label">{ZH_LABEL}</div>
            <div class="row-title">{ZH_TITLE}</div>
            <div class="row-desc">{ZH_DESCRIPTION}</div>
          </div>
          <span class="row-arrow">→</span>
        </a>
```

Then update, in both pages:

1. **The counter** in the index bar: `<span class="index-bar-label">{N} Presentations</span>`.
2. **`index_zh.html`** — use `href="{DECK_DIR}/index.html"` and Chinese copy.
3. **`index_en.html`** — use `href="{DECK_DIR}/index_en.html"` and English copy.
4. **`README.md`** — add the deck to both `Repo map` and `Decks`.

Note: `index.html` at the repo root is only a redirect stub to `index_en.html`; do not edit it.

---

## Step 6 — Companion docs

Recent decks ship a small, consistent doc set. Copy the pattern:

| File | Purpose |
|---|---|
| `README.md` | title, audience, timing table, file inventory, evidence boundaries |
| `source-map.md` | per-slide sources, engineering claims, image credits with Unsplash links |
| `qa/contact-sheet-zh.png` | flattened visual review sheet for the CN deck |
| `qa/contact-sheet-en.png` | flattened visual review sheet for the EN deck |

Keep image credits honest: name the photographer and link the Unsplash original. State plainly where content is synthetic or where no customer claim is implied.

---

## Step 7 — Verify

- New directory exists with both `index.html` and `index_en.html`.
- Both index pages contain the new row, and `row-num` runs `00`…`{N-1}` with no gaps.
- The "N Presentations" counter matches the row count.
- Every local `href` / `src` in the new deck resolves — reveal runtime, logos, and background images.
- `data-slide-id`s match one-to-one between the two languages, in the same order.
- `README.md` lists the deck in both `Repo map` and `Decks`.
- Remind the user to open the deck in a browser to check rendering.

---

## Shared asset reference

| Path | Contents |
|---|---|
| `assets/logo.svg` | Dify logo (used in all decks) |
| `agent-systems/styles.css` | Nordic design system (1300+ lines, vars + components) |
| `agent-plugin-governance/assets/reveal/` | Vendored reveal.js 4.5.0 — reuse instead of re-bundling |
| `enterprise-agent-campus/editorial.css` | Editorial grid + components (shared EN/CN base) |
| `enterprise-agent-campus/editorial-zh.css` | Chinese-only line-break, size, and rhythm calibration |
| `enterprise-agent-campus/assets/` | Localized Unsplash backgrounds, credited in `source-map.md` |
| `stripe-agent-workshop/editorial-en.css` | English editorial variant |
| `milvus/styles/dify-theme.css` | Milvus brand token overrides |
| `milvus/styles/base.css` | Milvus base typography + layout utilities |
| `milvus/styles/theme-swiss.css` | Sub-theme: Swiss minimal |
| `milvus/styles/theme-atelier.css` | Sub-theme: Atelier gradient |
| `milvus/styles/theme-ukiyo.css` | Sub-theme: Ukiyo washi |
| `aispeech/styles/nordic.css` | Pop Art base reset |
| `aispeech/styles/popart.css` | Pop Art component styles |

All CSS files are referenced via relative `../` paths from the deck directory — no copying needed.
