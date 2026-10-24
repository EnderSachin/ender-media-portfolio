# Ender Media website prototype

A responsive multi-page creator-editing studio website with a premium dark visual system.

## Pages
- `index.html` — portfolio landing page and Order CTA
- `services.html` — services
- `pricing.html` — proposed starting prices
- `samples.html` — sample gallery placeholders
- `signup.html` / `login.html` — demo client signup and login
- `order.html` — order intake, length-based estimate, references, brief and contact fields
- `admin.html` — demo operations dashboard, status changes, revenue/expenses, privacy blur, sample links, JSON export

## Run locally
Open `index.html` in a browser, or serve this folder using a local static web server. No build step is needed.

## Important limitations — do not mistake this for a production backend
This is a front-end prototype. Client accounts and orders are stored in `localStorage` in the same browser; passwords are not safely hashed, uploads are recorded as file metadata only, and the admin page has no authentication. Data will not sync across devices and is not secure. The admin dashboard seeds sample/demo orders when no orders exist. Do not publish this version with real client data.

Before launch, implement:
1. Server-side authentication (e.g. Supabase Auth) with admin-only authorization and row-level security.
2. Database tables for profiles, orders, order status history, studio expenses, and portfolio samples.
3. Secure object storage for uploaded files, signed URLs, file validation and size limits.
4. Server-side pricing validation, notifications, backups, rate limiting and privacy policy/consent.
5. Connect payments only after the final quote and delivery terms are defined.
6. Use your actual email, Discord, phone and domain; current brand is a design prototype.

## Pricing logic in this prototype
Base estimate by final length: under 30s ₹499; 30–60s ₹799; 1–3m ₹1,499; 3–8m ₹2,999; 8m+ ₹4,999. Advanced multiplier 1.7×, Premium 2.5×. Gaming adds ₹250, motion/custom adds ₹600, long-form adds ₹700. These are sample values; adjust before launch.


## UI update
The admin dashboard has a refined premium dark UI. The order-details close (×) button now closes via button, backdrop, or Escape. The financial hide toggle now reliably blurs money fields and remembers the preference in this browser.

## Premium all-pages UI update
All public pages (Portfolio, Services, Pricing, Samples, Signup, Login, Order) now share a consistent premium dark dashboard-inspired visual system with purple/pink accents, glassy panels, refined forms, hover states, and responsive mobile styling. Existing page content and JavaScript interactions are preserved.


## Contact & chat support prototype
- Open `admin.html` → Settings to edit Instagram, Discord, Gmail, WhatsApp, the chat greeting, and widget visibility.
- The public pages show a floating Chat support widget with the configured contact links. Sending a message opens WhatsApp (if configured), otherwise Gmail.
- This is a static prototype: settings are stored in browser localStorage, so admin edits do not sync to other visitors/devices on a deployed site. A shared backend/database is required for production-wide settings and real live chat.


## Uploaded video portfolio
The homepage and Samples page now display the 10 uploaded MP4 clips in a responsive gallery. Video files and poster thumbnails live in `media/`. Keep the `media` folder alongside `index.html` when deploying. Video playback is click-to-play and pauses other portfolio videos.


## Portfolio videos
The homepage and Samples page embed nine YouTube videos using privacy-enhanced YouTube embeds. Update the video IDs in `index.html` and `samples.html` if you want to replace a sample. The video files are hosted by YouTube, not bundled with this site.
