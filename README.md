# OneCardiology.com — Landing Page

Domain-for-sale landing page for onecardiology.com.

---

## Stack

- **Hosting**: Netlify (auto-deploys from GitHub on every push)
- **Repo**: https://github.com/jheimlich/onecardiology-landing
- **Form backend**: Formspree (https://formspree.io/f/mkoqddvr)
- **Captcha**: Cloudflare Turnstile
- **Domain registrar**: sav.com
- **DNS**: Netlify nameservers (dns1–dns4.p07.nsone.net)

---

## Making changes

Edit `index.html`, then:

```bash
git add index.html
git commit -m "your message"
git push
```

Netlify picks up the push and redeploys automatically (~30 seconds).

---

## Form submissions

Inquiries are delivered to brett.heimlich@gmail.com via Formspree.
You can also view all submissions at https://formspree.io under the OneCardiology form.

---

## Cloudflare Turnstile

- Site key is embedded in `index.html` in the `data-sitekey` attribute
- Secret key is stored in Formspree → form Settings
- To rotate keys: Cloudflare dashboard → Turnstile → OneCardiology site

---

## DNS setup (sav.com)

Nameservers are pointed to Netlify. Do not change these unless moving hosts.

```
dns1.p07.nsone.net
dns2.p07.nsone.net
dns3.p07.nsone.net
dns4.p07.nsone.net
```

SSL is managed automatically by Netlify (Let's Encrypt).

---

## To add a stock photo background

In `index.html`, find the `.hero` CSS rule and add:

```css
.hero {
  background-image: url('your-image-url');
  background-size: cover;
  background-position: center;
}
```

Recommended free sources: Unsplash, Pexels. Search "cardiology" or "medical abstract".
