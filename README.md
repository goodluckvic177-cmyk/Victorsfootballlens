# Victor's Football Lens: how to publish and update

## What is in this folder
- `index.html`, `news.html`, `players.html`, `fixtures.html`, `videos.html`, `about.html`: the pages
- `article.html`: the page that shows any single news story
- `js/data.js`: **all your content** (news, players, fixtures, results, videos). This is the only file you edit day to day.
- `css/style.css`: colours and design (red is `--red` at the top)
- `images/`: put your own pictures here (create the folder) and use them like `"images/story1.jpg"`

## Preview on your computer
Double-click `index.html`. It opens in your browser. No installation needed.

## Put it online for free (pick one)
**Netlify (easiest):** go to app.netlify.com/drop and drag this whole folder onto the page. You get a free web address in seconds. To update later, drag the updated folder again.

**Cloudflare Pages** or **GitHub Pages** also work and are free. Upload the folder contents so that `index.html` is at the top level.

When you buy a domain name, connect it in the hosting dashboard (Netlify and Cloudflare both guide you).

## Add a news story
1. Open `js/data.js` in any text editor (Notepad is fine).
2. Find `news: [`. Copy one whole story from `{` to `},`.
3. Paste it right under `news: [`, then change the id, title, date, text and so on.
4. Save, upload the folder again, done.

Rules: keep the quotes and commas. Each `id` must be unique, with no spaces. If something breaks, an extra or missing comma is nearly always the cause.

## Add a video
Upload to YouTube. From the link `youtube.com/watch?v=ABC123`, copy `ABC123` into `youtubeId`.

## Before you launch
1. In `data.js`, set your real `url`, `email` and social links.
2. In every `.html` file and in `sitemap.xml` and `robots.txt`, replace `https://www.victorsfootballlens.com` with your real address (use Find and Replace).
3. Replace all the sample text and add real stories, player notes, fixtures and videos.
4. Add a small logo image or favicon if you want one.
5. Submit your site in Google Search Console and upload `sitemap.xml`.

## Good to know
- **Images:** keep each under 300 KB (use squoosh.app) so the site stays fast.
- **SEO:** each page has its own title and description, and stories add structured data for Google. Because stories are shown by JavaScript from `data.js`, Google can read them but a plain-HTML site ranks slightly more reliably. If the site grows big, a good next step is moving to a generator such as Astro or Hugo, or a CMS, so each story gets its own permanent page.
- **Fixtures and scores** are entered by hand. For live scores you would later add a sports data service, which usually has a paid plan.
- **Player photos and club logos** are usually copyrighted. Use pictures you own or have permission to use.
