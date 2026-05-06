# AGENTS.md

Static HTML website for Shree Saraswati Secondary School (Satyawati, Gulmi, Nepal).

## Files

- `index.html` - Main website (~3175 lines, all inline)
- `admin.html` - Admin panel (~varies, localStorage + sessionStorage persistence)

## Tech Stack

- Vanilla HTML/CSS/JS (all inline, no build)
- Google Fonts (external CDN - requires internet)
- Images as base64 data URIs
- localStorage for data persistence, sessionStorage for admin login state

## Viewing

Open `index.html` or `admin.html` directly in any browser. No server or build required.

## Commands

- View site: Open HTML files directly in browser
- Generate architecture graph: Run graphify skill (see `opencode.json` plugin config)

## Key Sections (index.html)

| Section | HTML ID |
|---------|--------|
| Navbar/Hero | `#home` |
| About | `#about` |
| Academics | `#academics` |
| Stats | `#stats` |
| Teachers | `#teachers` |
| Notices | `#notices` |
| Gallery | `#gallery` |
| Events | `#events` |
| Admission | `#admission` |
| Contact | `#contact` |

## Admin Panel (admin.html)

- **Login**: Hardcoded credentials (see `admin.html:303-304`)
- **CRUD**: Teachers, Notices, Students (ECD through Grade 12), Statistics, Gallery, Settings
- **Admission Inquiries**: view-only
- **Persistence**: Admin settings in localStorage, sessionStorage for login state

## Key Field Details

- **Students**: Classes ECD-12 (Early Childhood Development through Grade 12)
- **Settings**: School name, phone, email, address, IEMIS code
- **Notices**: Categories include exam, admission, event

## Important Constraints

- **No lint, test, or build commands exist**
- **Admin credentials are embedded in source** (security consideration - not suitable for public hosting)
- index.html polls admin.html every 2s via localStorage for live updates (`index.html:2824`)
- graphify plugin regenerates architecture view at `graphify-out/GRAPH_REPORT.md`