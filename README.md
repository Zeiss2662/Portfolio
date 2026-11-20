# Zubair Mustafa — Academic & Professional Portfolio

A single-page, static website built with HTML5, CSS3 and vanilla JavaScript. No build step, no frameworks.

## Run locally

Open `index.html` in a browser. Google Fonts load online; the site falls back to Georgia and system fonts offline.

## Folder structure

```
Portfolio_Updated/
  index.html
  style.css
  script.js
  README.md
  assets/
    Zubair_Mustafa_CV.pdf        <- placeholder, replace with your CV
    images/                      <- hero, Hult Prize, summit, retreat photos
    projects/                    <- project covers
    certificates/                <- research acceptance notification
    icons/                       <- favicon
```

## Add your photographs

Save your files with exactly these names (JPG, ideally under 400 KB each; resize large photos to about 1600 px wide).
Until a file exists, the page shows a dashed placeholder box with its name.

| File | Used for |
|---|---|
| `assets/images/hero-portrait.jpg` | Hero: standing portrait in the blue blazer |
| `assets/images/hult-prize-committee.jpg` | Hult Prize organizing committee card |
| `assets/images/hult-prize-booth.jpg` | Hult Prize registration booth photo |
| `assets/images/data-science-summit-1.jpg` | Summit photo (hall with laptops) |
| `assets/images/data-science-summit-2.jpg` | Summit photo (poster display) |
| `assets/images/team-retreat.jpg` | Software Solution 360 retreat photo |
| `assets/projects/gantabya-cover.jpg` | Gantabya featured project card |
| `assets/certificates/icps-2026-acceptance.jpg` | Official ICPS 2026 acceptance notification |

Photos are already optimised and placed in `assets/`, except the ICPS acceptance notification, which was not supplied: save it as `assets/certificates/icps-2026-acceptance.jpg` (until then the Research section shows a dashed placeholder). The seated portraits and the group dinner photo are not used. Check the two summit photos: I assigned them to the National Data Science Summit entry; swap them if either is from another event.

## Branding note

The brief asked for a "BR" monogram, but the initials for Zubair Mustafa are ZM, so the logo and footer use ZM. To change it, search `monogram` in `index.html`.

## Things you must fill in

Search for `data-placeholder-link` in `index.html`. These links point to generic placeholders:

- **Email:** replace `your.email@example.com` (appears in Contact, footer and the Contact list; the form uses the first one).
- **GitHub:** replace `https://github.com/` and `github.com/your-username` (hero, contact, footer).

## Gantabya cover

The supplied Gantabya image has a slide caption baked in ("New Perspectives: Leadership for Tomorrow"). On desktop the card crops it out; on mobile the full image shows. For a cleaner look, replace `assets/projects/gantabya-cover.jpg` with a plain logo or app screenshot.

## Update the CV

Replace `assets/Zubair_Mustafa_CV.pdf` with your real CV, keeping the same file name. All "Download CV" buttons use it.

## Add project links

In the project cards, replace the line `Repository and demo links: not yet published` with:

```html
<a href="https://github.com/you/repo" target="_blank" rel="noopener">Repository</a>
```

Only add links that are live. To add a project, copy an existing `<article class="project">` and set `data-category` to `software`, `blockchain`, `iot` or `research` (separate several with spaces).

## Update the research status

After the poster has been presented, change the badge text in the Research section. The page currently says "Accepted — Poster Presentation" and makes no claim that it has been presented or published.

## Verify before publishing

- Education: the degree shows "Information and Communication Engineering" as specified in your brief. Your earlier site listed Software Engineering, so confirm which is correct.
- GPAs (HSC 5.00, SSC 4.89) come from your earlier education graphic. Remove them if you prefer not to show them.
- Employment dates are intentionally omitted. Add them to the timeline only when you have exact dates.

## Contact form

There is no backend. After client-side validation the form opens the visitor's email app (`mailto:`) with the message filled in. For real submissions, connect a service such as Formspree or Netlify Forms by setting the form's `action` and removing the `mailto` code in `script.js`.

## Deploy

- **GitHub Pages:** push the folder to a repository, then Settings > Pages > deploy from the main branch root.
- **Netlify / Cloudflare Pages:** drag and drop the folder or connect the repository (no build command, publish directory `/`).
- After deploying, change the `og:image` meta tag in `index.html` to the full URL (for example `https://yourname.github.io/assets/images/hero-portrait.jpg`) so link previews show your photo.

## Customise

Colors and spacing are CSS variables at the top of `style.css` (`:root` for light, `:root[data-theme="dark"]` for dark).
