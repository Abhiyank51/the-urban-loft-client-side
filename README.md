# The Urban Loft Cabins — Cabin Booking Website

A modern full-stack cabin booking website built with **Next.js 14**, **Supabase**, **NextAuth**, and **Tailwind CSS**. The application allows users to browse luxury cabins, view detailed cabin information, authenticate with Google, reserve cabins, manage bookings, and update their guest profile from a protected account area.

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![NextAuth](https://img.shields.io/badge/NextAuth-Authentication-purple?style=for-the-badge)

---

## Live Demo

**Deployed URL:** [https://the-urban-loft.vercel.app](https://the-urban-loft.vercel.app)

---

<p align="center">
  <img src="public/screenshots/home.png" alt="Home Page" width="48%" />
  <img src="public/screenshots/cabins.png" alt="Cabins Page" width="48%" />
</p>

<p align="center">
  <img src="public/screenshots/cabin-details.png" alt="Cabin Details Page" width="48%" />
  <img src="public/screenshots/account.png" alt="Guest Account Page" width="48%" />
</p>

---

## Features

- Browse a collection of luxury cabins with capacity-based filtering
- View individual cabin details, pricing, discount, capacity, and description
- Reserve cabins using an interactive date picker
- Google authentication using NextAuth
- Protected guest account area
- Create, update, and delete reservations
- Guest profile update with nationality, country flag, and national ID
- Supabase-powered data storage for cabins, bookings, guests, and settings
- Server Actions for secure booking and profile mutations
- Dynamic metadata and static generation for cabin detail pages
- Responsive and clean UI built with Tailwind CSS
- Custom loading, error, and not-found states

---

## Tech Stack

| Category | Technology |
|---|---|
| Framework | Next.js 14 |
| UI Library | React 18 |
| Styling | Tailwind CSS |
| Backend / Database | Supabase |
| Authentication | NextAuth v5 with Google Provider |
| Date Handling | date-fns, react-day-picker |
| Icons | Heroicons |
| Deployment | Vercel |

---

## Project Structure

```bash
the-wild-oasis-website/
├── app/
│   ├── _components/        # Reusable UI components
│   ├── _lib/               # Auth, Supabase client, data services, server actions
│   ├── _styles/            # Global styles
│   ├── account/            # Protected guest account pages
│   ├── api/                # API routes including NextAuth route
│   ├── cabins/             # Cabin listing, details, and reservation pages
│   ├── about/              # About page
│   ├── login/              # Login page
│   ├── layout.js           # Root layout
│   └── page.js             # Home page
├── public/                 # Static assets and screenshots
├── next.config.mjs         # Next.js image/domain configuration
├── tailwind.config.js      # Tailwind CSS configuration
├── package.json            # Project dependencies and scripts
└── README.md
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/abhiyank51/the-wild-oasis-website.git
cd the-urban-loft-website
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env.local` file in the project root:

```env
SUPABASE_URL=your_supabase_project_url
SUPABASE_KEY=your_supabase_service_or_anon_key
AUTH_GOOGLE_ID=your_google_oauth_client_id
AUTH_GOOGLE_SECRET=your_google_oauth_client_secret
AUTH_SECRET=your_nextauth_secret
```
---

## Run Locally

```bash
npm run dev
```

Open the app in your browser:

```bash
http://localhost:3000
```

---

## Build for Production

```bash
npm run build
npm start
```
---

## Main Pages

| Route | Description |
|---|---|
| `/` | Home page |
| `/about` | About the cabin retreat |
| `/cabins` | Cabin listing with filters |
| `/cabins/[cabinId]` | Cabin details and reservation form |
| `/login` | Google sign-in page |
| `/account` | Protected guest dashboard |
| `/account/profile` | Update guest profile |
| `/account/reservations` | Manage guest reservations |


---

## Supabase Tables Used

The application expects these main Supabase tables:

- `cabins`
- `bookings`
- `guests`
- `settings`

The cabin image URLs are loaded from Supabase Storage. The Supabase storage domain is configured in `next.config.mjs` for Next.js image optimization.

---

## Author

**Abhiyank Yadav**  
GitHub: [@abhiyankyadav51](https://github.com/abhiyankyadav51)
