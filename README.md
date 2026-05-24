# Spectral — Music & Mood Study

A browser-based research tool investigating whether frequency balance alone can influence emotional affect in music listening.

**Live site:** `https://[your-username].github.io/spectral-study`

---

## How It Works

Participants open the site, pick a track, and listen to three versions — Sad, Neutral, and Happy — each with a different EQ profile applied. After each version they rate how it made them feel. No installation required.

## Audio Files

Each source track is exported into three versions:

| File | Description |
|------|-------------|
| `trackname_sad.mp3` | Low shelf +9dB, high shelf −9dB, low-pass at ~1.4kHz |
| `trackname_neutral.mp3` | Unprocessed original |
| `trackname_happy.mp3` | High shelf +7dB, presence +5dB, volume ×1.5 |

## Adding More Tracks

1. Add `trackname_sad.mp3`, `trackname_neutral.mp3`, `trackname_happy.mp3` to `/audio/`
2. Add an entry to the `SONGS` array in `index.html`:

```js
{ id:"trackname", name:"Display Name", bpm:"120 BPM", key:"Am", type:"instrumental", label:"Genre" }
```

For vocal tracks set `type:"vocal"`.

## Setting Up the Google Form

1. Create your Google Form with the study questions
2. Copy the form URL
3. In `index.html`, replace `YOUR_FORM_ID_HERE` in the `FORM_URL` constant:

```js
const FORM_URL = "https://docs.google.com/forms/d/e/YOUR_FORM_ID/viewform";
```

## Deploying to GitHub Pages

1. Create a new GitHub repository
2. Upload all files (keep the `audio/` folder structure)
3. Go to Settings → Pages → Source → `main` branch → `/root`
4. Your site will be live at `https://[username].github.io/[repo-name]`

## Tracks

| Track | BPM | Key | Type |
|-------|-----|-----|------|
| Dill | 151 | C | Instrumental |
| Letter | 140 | Em | Instrumental |
| Miss | 140 | Gm | Instrumental |
| Aasu | 129 | Am | Instrumental |
| Roz | 146 | Am | Instrumental |
| Pole | 137 | Gm | Instrumental |

All tracks by Sravan Palla / Prodvyce. Used with permission for academic research.

## Credits

EQ processing based on Audio EQ Cookbook biquad filter formulas.  
Study design: Sravan Palla | Guide: Dr. Kamalakar Karlapalem | IIIT Hyderabad
