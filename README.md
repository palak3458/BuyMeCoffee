# BuyMeCoffee
A full-stack web application inspired by [BuyMeACoffee.com](https://www.buymeacoffee.com), allowing users to receive support in the form of donations. Built with **Next.js**, **TypeScript**, and **Tailwind CSS**, this app supports user authentication, profile customization, file uploads, and donation tracking.

---

## 🚀 Project Overview

This project mimics the core functionality of Buy Me a Coffee:
- Users can register or log in using secure authentication.
- Visitors can donate to support a user's work.
- Users can personalize their profile and view donation status.
- Implements file uploads for profile/media handling.

---

## 📁 Folder Structure

```plaintext
public/
  ├── next.svg
  └── vercel.svg         # Static assets

src/
├── actions/             # Server-side actions like donation, uploads, and profile updates
│   ├── donationActions.ts
│   ├── profileInfoActions.ts
│   └── uploadActions.ts

├── app/                 # Next.js App Router structure
│   ├── [username]/      # Dynamic routing for user profile pages
│   │   └── page.tsx
│   ├── about/           # About page
│   │   └── page.tsx
│   ├── api/auth/[...nextauth]/route.ts  # NextAuth API route
│   └── callback/route.ts               # OAuth callback handling
│   └── profile/page.tsx               # User profile page

components/
  ├── DonationForm.tsx
  ├── DonationStatus.tsx
  ├── Header.tsx
  ├── ProfileInfoForm.tsx
  └── UploadButton.tsx

lib/
  ├── authOptions.ts     # NextAuth configuration
  └── db.ts              # Database connection logic

models/
  └── (Assumed: Contains database schemas)

root files:
  ├── next.config.mjs
  ├── tailwind.config.ts
  ├── tsconfig.json
  ├── postcss.config.mjs
  ├── globals.css
  ├── .eslintrc.json
  └── README.md (this file)
````

---

## 🛠️ Technologies Used

| Technology               | Purpose                    |
| ------------------------ | -------------------------- |
| **Next.js 13+**          | Full-stack React Framework |
| **TypeScript**           | Type-safe development      |
| **Tailwind CSS**         | Utility-first styling      |
| **NextAuth.js**          | Authentication with OAuth  |
| **PostgreSQL** (assumed) | Backend database           |
| **Prisma** (assumed)     | ORM for DB interaction     |
| **Vercel**               | Hosting and deployment     |

---

## 💡 Features

* 🔒 **Authentication**: Secure login with OAuth (NextAuth)
* 👤 **Dynamic Profiles**: `/[username]` routes show personalized pages
* ☕ **Donation System**: Easily support creators with one-time payments
* 📤 **File Uploads**: Allow users to upload images/media
* 🧾 **Donation Status**: View recent donations per user
* 🎨 **Custom UI**: Built using Tailwind CSS

---

## 📌 How It Works

1. **User Registration/Login** via OAuth.
2. **Profile Creation**: Users can customize their info and image.
3. **Donation Page**: Public page where others can send support.
4. **Backend Actions**:

   * `donationActions.ts`: Handles payment logic
   * `uploadActions.ts`: Manages file uploads
   * `profileInfoActions.ts`: Manages profile updates
5. **Components**: Modular UI components like `Header`, `DonationForm`, etc.
6. **API Routes**: Custom routes for authentication and callbacks.

---

## 🔭 Future Scope

* ✅ Email Notifications on donations
* ✅ Add Stripe/PayPal integration
* 📈 Analytics for donation trends
* 📬 Direct messaging between supporters and creators
* 🎁 Subscription-based support model
* 🌐 Internationalization (i18n)

---

## 📣 Getting Started

### 1. Clone the repo

```bash
git clone this repo
cd buymeacoffee-clone
```

### 2. Install dependencies

```bash
pnpm install
```

### 3. Set up environment variables

Create a `.env.local` and add:

```env
DATABASE_URL=your_database_url
NEXTAUTH_SECRET=your_secret
NEXTAUTH_URL=http://localhost:3000
GITHUB_ID=your_github_id
GITHUB_SECRET=your_github_secret
```

### 4. Run the development server

```bash
pnpm dev
```

Visit `http://localhost:3000` 🚀

---

## 📄 License

MIT License. Free for personal and commercial use.

---

## ✨ Credits

Built with ❤️ using Next.js, Tailwind, and a passion


```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
