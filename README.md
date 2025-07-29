
# 🔗 My Self-Hosted LittleLink Site – `chamb.dev`

This project is a self-hosted version of **[LittleLink](https://github.com/sethcottle/littlelink)** — a lightweight, open-source alternative to Linktree — deployed using Docker and connected to my custom domain, [chamb.dev](https://chamb.dev).

I cloned the original LittleLink repository, customized the layout, and containerized the app using Docker for easy local and remote deployment. The site is hosted through **GitHub Pages** and mapped to my **GoDaddy domain** using proper DNS records.

---

## 🧰 What I Used

- 🐙 GitHub for version control and static hosting
- 🐳 Docker for containerizing the app
- 🌐 GoDaddy to manage DNS for my custom domain
- 💻 LittleLink for front-end design and link hub layout

---

## ⚙️ How I Built It

### 1. Cloned the LittleLink Repository

```bash
git clone https://github.com/sethcottle/littlelink.git
cd littlelink
```

> I created a fork of the repo to personalize my page and branding.

---

### 2. Customized the Content

I edited the `index.html` file to include my own links (GitHub, portfolio, social media), and adjusted the styles in `style.css` and `css/brands.css` to match my personal theme.

---

### 3. Dockerized the Project

I created a simple `Dockerfile` to serve the static site using Nginx:

```dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
```

Then I built and ran the container:

```bash
docker build -t littlelink .
docker run -d -p 80:80 littlelink
```

This served the site locally, making testing and iteration fast and consistent.

---

### 4. Connected to My Domain (`chamb.dev`)

In GoDaddy’s DNS manager, I set up the following records:

| Type  | Name | Value (example)           | TTL     |
|-------|------|----------------------------|---------|
| A     | @    | `185.199.108.153` (GitHub) | Default |
| A     | @    | `185.199.109.153`          | Default |
| A     | @    | `185.199.110.153`          | Default |
| A     | @    | `185.199.111.153`          | Default |
| CNAME | www  | `chambsec.github.io`       | Default |

> I also added a `CNAME` file in the repo that includes `chamb.dev` to tell GitHub Pages which domain to use.

---

## 🌈 Features

- 100+ branded button styles included
- Easy customization via HTML and CSS
- Built-in dark/light/auto themes
- Accessibility enhancements (contrast and visibility)
- Docker support for clean, repeatable deployments
- Compatible with GitHub Pages, Netlify, Vercel, and AWS Amplify

---

## 📊 Performance

LittleLink is optimized for speed and simplicity. My deployed page scores a perfect 100/100 across all categories on Google PageSpeed Insights — including performance, SEO, accessibility, and best practices — thanks to its clean, no-framework build.

---

## 🌐 Live Site

👉 [https://chamb.dev](https://chamb.dev)

---

## 🙋‍♂️ About Me

**Chris Chambers**  
Cybersecurity | Cloud Enthusiast  
🔗 [GitHub](https://github.com/chambsec) | 🌐 [chamb.dev](https://chamb.dev)

---

## 🧱 Credit

This project is based on [LittleLink](https://github.com/sethcottle/littlelink) by [Seth Cottle](https://github.com/sethcottle), licensed under MIT.
