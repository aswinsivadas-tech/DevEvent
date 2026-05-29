````md
# DevEvent

A modern full-stack event management platform built with Next.js 16, MongoDB, Tailwind CSS v4, and TypeScript.  
DevEvent allows users to create, manage, and explore developer-focused events with a clean and responsive UI.

---

# Features

- Create and manage tech events
- MongoDB database integration with Mongoose
- Dynamic event pages using slugs
- Tailwind CSS v4 styling
- Responsive modern UI
- TypeScript support
- Server-side rendering with Next.js App Router
- Event validation and normalization
- Automatic slug generation
- Cloudinary image support
- PostHog analytics integration

---

# Tech Stack

## Frontend
- Next.js 16
- React 19
- TypeScript
- Tailwind CSS v4

## Backend
- Next.js Server Actions / API Routes
- MongoDB
- Mongoose

## Other Tools
- Cloudinary
- PostHog
- Lucide React
- clsx
- tailwind-merge

---

# Project Structure

```bash
devevent/
│
├── app/
│   ├── api/
│   ├── events/
│   ├── globals.css
│   └── layout.tsx
│
├── components/
│
├── database/
│   └── event.model.ts
│
├── lib/
│   └── mongodb.ts
│
├── public/
│
├── .env.local
├── package.json
└── README.md
````

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/devevent.git
cd devevent
```

---

## 2. Install Dependencies

```bash
npm install
```

---

# Environment Variables

Create a `.env.local` file in the root directory.

```env
# MongoDB
MONGODB_URI=your_mongodb_connection_string

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# PostHog
NEXT_PUBLIC_POSTHOG_KEY=your_posthog_key
NEXT_PUBLIC_POSTHOG_HOST=https://app.posthog.com
```

---

# Running the Project

## Development Server

```bash
npm run dev
```

Visit:

```bash
http://localhost:3000
```

---

# Build for Production

```bash
npm run build
```

---

# Start Production Server

```bash
npm start
```

---

# Event Model Features

The event schema includes:

* Title validation
* Description validation
* Slug auto-generation
* Date normalization
* Time normalization
* Automatic timestamps
* Unique slug handling
* Compound indexing

---

# Example Event Data

```json
{
  "title": "Frontend Developer Conference",
  "description": "A large-scale developer conference focused on frontend technologies.",
  "overview": "Learn React, Next.js, and performance optimization.",
  "image": "https://example.com/banner.jpg",
  "venue": "Tech Convention Center",
  "location": "San Francisco, CA",
  "date": "2026-01-31",
  "time": "13:00",
  "mode": "offline",
  "audience": "Frontend Developers",
  "agenda": [
    "Keynote Session",
    "React Workshop",
    "Networking"
  ],
  "organizer": "DevEvent Team",
  "tags": [
    "React",
    "Next.js",
    "Frontend"
  ]
}
```

---

# Tailwind CSS Setup

This project uses Tailwind CSS v4.

Example `globals.css`:

```css
@import "tailwindcss";
@import "tw-animate-css";
```

---

# Common Issues

## Tailwind Styles Not Loading

Make sure:

```bash
npm install tw-animate-css
```

and inside `globals.css`:

```css
@import "tailwindcss";
@import "tw-animate-css";
```

---

## MongoDB URI Error

Ensure `.env.local` contains:

```env
MONGODB_URI=your_connection_string
```

Restart the development server after updating environment variables.

---

## Duplicate Schema Index Warning

Remove duplicate slug index definitions.

Do NOT use both:

```ts
slug: {
  unique: true
}
```

and

```ts
EventSchema.index({ slug: 1 }, { unique: true });
```

Use only one.

---

# Scripts

```json
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "eslint"
}
```

---

# Future Improvements

* Authentication
* User dashboard
* Event registration
* Payment integration
* Admin panel
* Search and filters
* Email notifications
* Event analytics

---

# Author

Aswin Sivadas

---

# License

This project is licensed under the MIT License.

```
```
