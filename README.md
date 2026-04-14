# Serenity — Mental Health Platform

A complete, fully functional mental health platform built with vanilla HTML, CSS, and JavaScript.
No frameworks. No build tools. Just open `index.html` in a browser.

---

## 📁 Project Structure

```
serenity/
├── index.html              ← Main entry point (all HTML)
│
├── css/
│   ├── variables.css       ← CSS custom properties, reset, keyframes
│   ├── components.css      ← Nav, buttons, toasts, footer, shared UI
│   ├── landing.css         ← Hero, features, matching, tools, CTA
│   ├── app.css             ← Dashboard, sidebar, all app pages
│   ├── modals.css          ← Modal overlays, forms, assessment, booking
│   └── responsive.css      ← Media queries (mobile / tablet)
│
└── js/
    ├── data.js             ← DB helper, static data (therapists, resources, posts)
    ├── ui.js               ← Modals, toasts, navigation, scroll reveal
    ├── auth.js             ← Login, register, demo login, logout
    ├── dashboard.js        ← Dashboard stats, upcoming appointments, mood mini-chart
    ├── mood.js             ← Mood selection, save, history list, 7-day chart
    ├── journal.js          ← Journal CRUD (create, read, update, delete)
    ├── therapists.js       ← Therapist cards, filtering, booking calendar & time slots
    ├── appointments.js     ← Upcoming / past appointments, cancel, join session
    ├── assessment.js       ← 5-step AI matching wizard + results
    ├── chat.js             ← AI support chat via Anthropic Claude API
    └── community.js        ← Community forum posts + resource library
```

---

## 🚀 Getting Started

1. **Clone / download** this folder.
2. Open `index.html` directly in any modern browser — no server required.
3. Click **Get Started** or **Continue as Guest (Demo)** to explore.

> **Note:** The AI Support Chat (`js/chat.js`) calls the Anthropic API directly from the browser.
> The API key is handled by the Claude.ai environment. If running outside Claude.ai, you will
> need to add your own API key or route requests through a backend proxy.

---

## ✅ Features

| Feature | Description |
|---|---|
| **Auth** | Register, sign in, session persistence via localStorage, guest/demo mode |
| **Dashboard** | Live stats (sessions, journal entries, mood average), mini mood chart, upcoming appointments |
| **Mood Tracker** | Emoji mood picker (1–5), optional note, 7-day bar chart, full history list |
| **Journal** | Full CRUD editor — create, read, update, delete entries; sidebar list |
| **Find a Therapist** | 6 therapists with filter chips (anxiety, depression, trauma, CBT, etc.) |
| **AI Assessment** | 5-step wizard that matches answers to the best therapist with a % score |
| **Appointment Booking** | 14-day calendar picker, time slots, session type, notes field |
| **Appointments** | Upcoming & past sessions, cancel, join (marks as completed) |
| **AI Support Chat** | Powered by Claude (Sonnet) — empathetic "Sage" persona, typing indicator, crisis reminders |
| **Community** | Seed posts + create anonymous posts, filter by category |
| **Resource Library** | 8 curated cards (meditation, CBT exercises, articles, videos) |
| **Crisis Support** | Persistent banner + modal with 988 Lifeline, Crisis Text Line, 911 |
| **Responsive** | Adapts to tablet and mobile breakpoints |

---

## 🗄️ Data Storage

All user data is stored in **localStorage** under namespaced keys:

| Key pattern | Contents |
|---|---|
| `sry_user` | Current logged-in user object |
| `sry_users` | All registered users (keyed by email) |
| `sry_{userId}_moods` | Array of mood entries |
| `sry_{userId}_journal` | Array of journal entries |
| `sry_{userId}_appointments` | Array of appointment objects |
| `sry_{userId}_posts` | Community posts created by this user |

---

## 🤖 AI Chat Configuration

The chat system prompt lives in `js/chat.js` as `CHAT_SYSTEM`.
To change the AI's persona, tone, or instructions — edit that constant.

```js
// js/chat.js
const CHAT_SYSTEM = `You are a compassionate mental health support companion named Sage...`;
```

---

## 🎨 Design Tokens

All colours and design values are CSS custom properties in `css/variables.css`:

```css
:root {
  --sage:       #7a9e87;
  --sage-light: #b5cebf;
  --sage-dark:  #4a6b56;
  --warm:       #f5efe8;
  --clay:       #c4836a;
  --deep:       #1c2b24;
  /* ... */
}
```

---

## ⚠️ Disclaimer

This platform is a demonstration project. The AI chat is **not** a substitute for professional mental health care.
If you or someone you know is in crisis, please contact:

- **988 Suicide & Crisis Lifeline** — call or text 988
- **Crisis Text Line** — text HOME to 741741
- **Emergency services** — call 911

---

© 2026 Serenity Health, Inc.
