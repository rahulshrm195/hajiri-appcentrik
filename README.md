# Hajiri — Attendance Manager

> Multi-business attendance, advances, and payroll management SaaS PWA

**Live:** [hajiri.appcentrik.in](https://hajiri.appcentrik.in)  
**By:** AppCentrik · Rahul Shrm

---

## What is Hajiri?

Hajiri (हाजिरी) is a multi-tenant SaaS PWA for managing daily wage employee attendance, advances, and payroll. Any business can sign up, create their Business ID, and start managing their team instantly — for free.

---

## Features

- 🏢 **Multi-tenant** — Each business gets isolated data under their own Business ID
- 📋 **Daily Mark** — Bulk attendance marking for all staff with ← → date navigation
- 💰 **Inline Advances** — Record advances alongside attendance in one Save All
- 📝 **Remarks** — Per-employee per-day notes for accountability
- 📒 **Ledger** — Running account per employee with opening balance, settlements, PDF export
- 📊 **Hisab Report** — Month-by-month summary with inline wage editing, full detail drill-down
- 📅 **Calendar** — Visual color-coded monthly attendance calendar
- 💼 **Wage History** — Different wage rates for different date periods
- ⏸ **Deactivate** — Hide employees who have left, reactivate when they return
- 🌗 **Dark / Light / Auto** mode
- 📄 **PDF exports** — Ledger, Hisab summary, Month detail
- ⌨️ **Keyboard navigation** — Full keyboard support on Daily Mark (desktop)
- 🔐 **Super Admin** — Access via `?superadmin` to manage all businesses

---

## Tech Stack

- Single-file HTML PWA (no build step)
- Firebase Firestore (`all-appcentrik` project)
- GitHub Pages hosting
- jsPDF for PDF generation

---

## Firestore Structure

```
businesses/{businessId}/
  ├── profile (businessName, ownerName, phone, createdAt)
  ├── users/{userId}
  ├── attendance/{userId}
  ├── advances/{advId}
  ├── requests/{reqId}
  └── notifications/{notifId}
```

---

## Deployment

1. Upload `index.html`, `sw.js`, `manifest.json`, `offline.html`, `icon-192.png`, `icon-512.png` to GitHub Pages
2. Set CNAME to `hajiri.appcentrik.in`
3. Update Firestore rules

---

*Built by AppCentrik · Part of the Amar Group ecosystem*
