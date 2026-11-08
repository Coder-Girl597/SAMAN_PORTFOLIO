# SAMAN_PORTFOLIO
A premium, minimal, fully responsive personal portfolio for **Saman Shakeel**, Social Media Manager and Automation Specialist based in Rawalpindi, Pakistan. Built to be shared with international clients, remote employers and freelance leads.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Responsive](https://img.shields.io/badge/Responsive-yes-8E7FBF)
![No build step](https://img.shields.io/badge/Build%20step-none-8E7FBF)

**Live site:** `https://coder-girl597.github.io/Sam_Portfolio-/` (available once GitHub Pages is turned on, see [Deploy](#deploy-with-github-pages))

---

## Features

- **Hero** with name, title, headline and call-to-action buttons
- **About Me** with bio, education, location and work preference
- **Services**: six cards covering Virtual Assistance, Social Media Management, Graphic Design, Video Editing, AI & Workflow Automation and Web Designing
- **Featured Projects**: AI Email Summarizer & Priority Classifier, and AI Social Media Content Generator & Scheduler
- **Social Media Posts**: a swipeable slider of Instagram and Facebook designs and a carousel video
- **Reels & Shorts**: vertical 9:16 video cards
- **Skills & Tools** grouped by category
- **Contact form** that delivers messages to email, plus direct email and LinkedIn links
- **Light and dark theme toggle**, remembered per visitor
- Click-to-enlarge images, smooth scrolling, subtle animations (disabled for visitors who prefer reduced motion)
- Semantic HTML, keyboard-friendly controls, SEO title and meta description

## Tech stack

Plain **HTML, CSS and JavaScript** in a single `index.html`. No frameworks, no build step, nothing to install. Fonts (Fraunces and DM Sans) load from Google Fonts with system-font fallbacks.

## Repository structure

```
.
├── index.html                  # The whole website
├── videos/
│   ├── carousel-video.mp4      # Social Media Posts slider
│   ├── mobile-video.mp4        # Reels & Shorts
│   └── advertising-video.mp4   # Reels & Shorts
└── README.md
```

`index.html` must stay at the top level of the repository for GitHub Pages to find it.

## Run locally

Download or clone the repository, then open `index.html` in any modern browser. Keep the `videos` folder next to it.

```bash
git clone https://github.com/Coder-Girl597/Sam_Portfolio-.git
cd Sam_Portfolio-
# open index.html in your browser
```

## Deploy with GitHub Pages

**Without the command line**

1. Sign in to GitHub and click **New repository**. Give it a name and make it **Public**.
2. Click **uploading an existing file**. Drag in `index.html`, the `videos` folder and `README.md`, then click **Commit changes**.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, then click **Save**.
5. Wait a minute or two. Your site appears at `https://coder-girl597.github.io/Sam_Portfolio-/`.

**With git**

```bash
git init
git add .
git commit -m "Add portfolio"
git branch -M main
git remote add origin https://github.com/Coder-Girl597/Sam_Portfolio-.git
git push -u origin main
```

Then follow steps 3 to 5 above.

**Tip:** name the repository `Coder-Girl597.github.io` to get the shorter address `https://coder-girl597.github.io/`.

Netlify and Cloudflare Pages also work: upload the same files.

## Contact form setup

The form sends messages through [Web3Forms](https://web3forms.com), which forwards them to your email.

1. Get a free access key at web3forms.com using your email address.
2. In `index.html`, find these lines near the top of the script and add your values:

```js
const FORM_ENDPOINT = "https://api.web3forms.com/submit";
const ACCESS_KEY = "your-access-key-here";
```

Web3Forms access keys are designed to be public, so it is safe for the key to sit in a public repository. After deploying, send a test message and check your inbox, including spam.

If `FORM_ENDPOINT` is left empty, the form only opens the visitor's email app, and nothing is delivered unless they press send there.

## Updating content

Open `index.html` and search for **`EDIT HERE`**. Your content lives in a few lists at the top of the script.

**Projects** (`PROJECTS`)

```js
{ title: "Project name",
  desc: "Short description.",
  features: ["Feature one", "Feature two"],
  tools: ["n8n", "Google Sheets"],
  steps: ["Step 1", "Step 2"],
  shot: "images/project.jpg",   // screenshot path
  link: "" }                    // add a real URL to show a "View Project" button
```

**Social media posts** (`POSTS`): each line is a slide.

```js
{ type: "image", src: "images/post1.jpg", alt: "Short description" },
{ type: "video", src: "videos/my-carousel.mp4", poster: "images/poster.jpg", alt: "Short description" }
```

**Reels and Shorts** (`REELS`)

```js
{ title: "Video title", platform: "Instagram Reels", src: "videos/my-reel.mp4", poster: "images/poster.jpg", link: "" }
```

Use `src` for a video file that plays on the page, or `link` to open the video on Instagram, Facebook or YouTube instead.

**Swapping embedded images:** some images are embedded inside `index.html` as long `data:image/...` text so the site works as one file. To replace one, swap that text for a normal path such as `images/post1.jpg` and add the image to an `images` folder next to `index.html`.

**Colors and fonts:** the palette is defined once at the top of the `<style>` block (`--bg`, `--card`, `--ink`, `--lav` and so on), with a second set for dark mode.

## Good practice

- Keep images and videos small. Around 720p video loads much faster.
- Only show real work and real results. Avoid invented client names, statistics or links.
- Check that any client work you show is approved for public display, especially if it shows phone numbers or addresses.

## Contact

**Saman Shakeel**
Email: [s.samsha.ja@gmail.com](mailto:s.samsha.ja@gmail.com)
LinkedIn: [saman-shakeel-ws592001](https://www.linkedin.com/in/saman-shakeel-ws592001/)
Location: Rawalpindi, Pakistan · Remote / Freelance
