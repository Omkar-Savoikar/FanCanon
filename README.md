# 📚 FanCanon

**FanCanon** is a blazing-fast, SEO-friendly static web app to explore canonical characters from all your favorite franchises — Marvel, DC, Anime, Cartoons, Games, and more.

---

## 🚀 Tech Stack

- **Framework**: [Next.js](https://nextjs.org/) (App Router + Static Site Generation)
- **Deployment**: [Vercel](https://vercel.com/)
- **Email**: [Nodemailer](https://nodemailer.com/) via serverless API route
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Components**: [shadcn](https://ui.shadcn.com/)
- **Search**: [Fuse.js](https://fusejs.io/) (client-side fuzzy search)

---

## 🔧 Features

- 🔍 Browse characters by franchise
- 📄 SEO-optimized static character pages
- 📬 Character/franchise request form (sends email to admin)
- ⚡ Fast performance with CDN edge deployment
- ✅ Mobile-first, accessible design (WCAG friendly)

---

## 📂 Project Structure

```txt
/fancanon
├── public/ # Images, favicon, OG banners
└── src/
    ├── app/
    │   ├── page.tsx # Homepage
    │   ├── request/page.tsx # Email request form
    │   ├── [franchise]/page.tsx # Franchise landing page
    │   └── [franchise]/[character]/page.tsx # Character detail page
    ├── api/
    │   └── request.ts # Nodemailer API handler
    ├── lib/
    │   └── data.json # Static content (or dynamic import)
    └── components/ # Reusable UI components
```

---

## 📬 Setup Email (Nodemailer)

1. Enable **App Passwords** in Gmail (or use an SMTP provider like Mailgun/Resend).
2. Add the following to your `.env.local`:

    ```env
    MAIL_USER=your_email@gmail.com
    MAIL_PASS=your_app_password
    RECEIVER_EMAIL=your_destination_email@gmail.com
    ```

3. Add the same keys in Vercel → Project Settings → Environment Variables.

---

## 🛠️ Local Development

```bash
npm install
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000)

---

## ✨ Roadmap

- Timeline viewer for characters
- Compare characters across universes
- Canon vs non-canon toggle
- Dynamic OG image generation (Vercel OG or Satori)

---

## 🙌 Contributing

Currently a solo project. Feature or character requests are welcome via the request form on the site.

---

## 📄 License

[MIT](./LICENSE)
