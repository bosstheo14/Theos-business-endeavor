# Launch Local: website storefront (static site)

Plain HTML/CSS/JS, no build step. Deploys on Netlify. Payments via Stripe Payment Links.

## Make it yours (do these before launch)
1. Brand: search/replace "Launch Local" in all .html files with your new name.
2. Email: replace hello@yourdomain.com in contact.html and terms.html.
3. Prices, turnaround times, and what each package includes: only promise what you can deliver.
4. Terms: terms.html is a template with [brackets]. Fill it in and have it reviewed before taking money.
5. Add real testimonials and portfolio pieces only when you have them. Do not invent reviews.

## Stripe setup
1. Create a Stripe account and finish activation.
2. Dashboard -> Payment links -> create one link per button:
   - Starter / Business / Growth: one 50% deposit link and one pay-in-full link each (6 links).
   - Care plan: a recurring monthly link, if you offer it.
3. For each link, under "After payment", choose "Don't show confirmation page" and
   redirect to https://YOURDOMAIN/welcome so buyers land on your intake form.
4. Paste each link into index.html and pricing.html, replacing the REPLACE_WITH_... URLs.
5. Make a small test payment with Stripe test mode first.

## Deploy
1. Push to a new GitHub repo (index.html must be at the repo root).
2. Netlify -> Add new project -> Import from Git. Leave build command empty.
3. Domain management -> Add a custom domain -> your new domain.
   - If the domain is registered at Namecheap, either switch its nameservers to Netlify DNS
     (Netlify shows the 4 nameservers) or add the DNS records Netlify lists.
4. Netlify Forms: after deploying, enable email notifications under Forms so you get messages.
