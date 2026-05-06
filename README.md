# portfolio-data

Static assets for [therakiburkhan.dev](https://therakiburkhan.dev) — JSON data files and images served via jsDelivr CDN.

---

## Structure

```
portfolio-data/
├── data/
│   ├── hero.json       ← name, typed items
│   ├── social.json     ← social links
│   ├── about.json      ← bio, dob, degree, city, phone, email
│   ├── skills.json     ← skills with levels
│   ├── resume.json     ← summary, education, experience
│   └── contact.json    ← location, email, phone
├── img/
│   ├── profile.jpg     ← profile photo
│   └── projects/
│       └── *.jpg       ← project screenshots
└── README.md
```

---

## CDN URL

Files are served via jsDelivr:

```
https://cdn.jsdelivr.net/gh/TheRakiburKhan/portfolio-data@main/{path}
```

Examples:

```
https://cdn.jsdelivr.net/gh/TheRakiburKhan/portfolio-data@main/data/hero.json
https://cdn.jsdelivr.net/gh/TheRakiburKhan/portfolio-data@main/img/profile.jpg
```

---

## How to Update

### Update JSON data

1. Edit the relevant file in `data/`
2. Commit and push to `main`
3. Live on site within 24h (jsDelivr cache)

```bash
git add data/resume.json
git commit -m "update resume"
git push
```

### Add or replace an image

1. Drop the new file into `img/`
2. Commit and push to `main`
3. Live on site within 24h

```bash
git add img/profile.jpg
git commit -m "update profile photo"
git push
```

---

## Notes

- Repo must stay **public** for jsDelivr to serve files
- 24h CDN cache lag is expected — updates are not instant
- Do not rename files without updating `data.js` in the main site repo
