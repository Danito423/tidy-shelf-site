# The Tidy Shelf — starter site

A 3-page starter site for a Home & Kitchen Amazon affiliate blog:

- `index.html` — homepage (hero, categories, featured picks, blog list, Pinterest CTA)
- `blog-post.html` — sample article template with product callouts
- `disclosure.html` — required affiliate disclosure + about page
- `style.css` — all styling, one shared file

## 1. Get your Amazon Associate links

1. Sign up at [affiliate-program.amazon.com](https://affiliate-program.amazon.com).
2. Once approved, use Amazon's **SiteStripe** toolbar (appears on Amazon product pages once you're logged into Associates) to grab a short link for each product.
3. In `index.html` and `blog-post.html`, find every `<a href="#" class="see-link">See on Amazon</a>` and replace the `#` with your real link.
4. Keep the disclosure text in the footer and on `disclosure.html` — Amazon requires it on every page with affiliate links, and the FTC requires it near the links themselves.

## 2. Connect Pinterest

1. Create a **Pinterest Business account** (free) and switch your existing account if needed, at business.pinterest.com.
2. **Claim your website**: Pinterest settings → Claim → add the domain. It gives you a meta tag — paste it into the commented-out line near the top of `index.html`:
   ```html
   <meta name="p:domain_verify" content="YOUR_VERIFICATION_CODE">
   ```
3. Turn on **Rich Pins** (Settings → Rich Pins) so pins from your site auto-pull the title and description.
4. Replace `https://pinterest.com/` in the "Follow on Pinterest" and footer links with your actual profile URL.
5. When you pin from your own articles, Pinterest will use the page's `<meta name="description">` — already set on each page — as the pin description.

## 3. Publish it

Easiest free options, no server needed:
- **Netlify** — drag the whole folder into app.netlify.com/drop.
- **GitHub Pages** — push the folder to a GitHub repo, enable Pages in repo settings.
- **Vercel** — `vercel` CLI or drag-and-drop via their dashboard.

Any of these will give you a live URL you can use for Pinterest's domain claim step.

## 4. Add more content

- Duplicate `blog-post.html` for each new article, update the title/meta/kicker/date, and add it as a new `.post-row` link in `index.html`'s blog section.
- Duplicate a `.pick-card` block in `index.html` for each new featured product.
- Keep articles specific ("9 ways to free up counter space in a small kitchen") rather than generic ("kitchen organization tips") — it performs better on both Pinterest and search.

## Notes

- No tracking/analytics included — add Google Analytics or Plausible if you want visitor data.
- No images are included (all icons are hand-drawn SVG). Add real product photos to the `.pick-card` elements and Pinterest-ready vertical images (1000×1500px works well) to blog posts once you have them.
