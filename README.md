# Community Engineering Project Website

Static site: HTML5, CSS3, vanilla JavaScript. No build step, no frameworks.

## Run locally
Open `index.html` in a browser, or serve the folder:
`python3 -m http.server 8000` then visit http://localhost:8000
(Google Fonts load from the internet; the site falls back to system fonts offline.)

## Set your organization details
1. **Edit `js/main.js`, the `ORG_CONFIG` block at the top.** Name, email, phone, location, hours, map URL and form endpoint update on every page. Empty fields keep their visible placeholder.
2. Search the four HTML files for `Your Organization` and update `<title>`, meta and Open Graph tags (these are static for SEO).
3. Replace the placeholder text, sample projects, team cards and impact figures with real content.

## Impact numbers
Values are placeholders. Replace them with verified figures, set `data-count` to the number and `data-verified="true"` to enable the count-up.

## Connect the contact form
`js/forms.js` validates the form. Until `formEndpoint` is set it runs in **demo mode** and clearly says nothing was sent.
To go live: create a form on Formspree, Web3Forms or Getform, then paste its URL into `formEndpoint` in `js/main.js`. A success message appears only when the service returns a successful response.
Links such as `contact.html?type=volunteer` preselect the enquiry type (`general, volunteer, donation, partnership, food-services, other`).

## WhatsApp and map
The WhatsApp button stays hidden until a valid phone number is set. Paste a Google Maps "Embed a map" `src` URL in `mapEmbedUrl` to show a map.

## Images and replacement
Images in `assets/images/` (JPG) were supplied for Annasetu:

| File | Used for |
|---|---|
| hero-community.jpg | Home hero, Food Services outreach card, social preview image |
| volunteers-food-supplies.jpg | Food Services hero, home card, About story |
| community-volunteers.jpg | Home About split, project card, meal distribution |
| donation-box.jpg | Food Redistribution card, surplus collection |
| hands-globe.jpg | Sustainable Communities card |
| hunger-relief.jpg | Sample project card, partnerships |
| shared-hearts.jpg | About hero, sample project card |

Keep the `width`/`height` attributes and a descriptive `alt` when swapping. Only use images you own or are licensed to use, and get consent for photos of people. `assets/logo.svg` is a placeholder mark; replace it with Annasetu's own logo.

## Structure
`index.html about.html food-services.html contact.html`, `css/` (style, responsive, animations), `js/` (main, navigation, forms), `assets/`.
