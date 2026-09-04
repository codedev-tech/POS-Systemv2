# POS System v2

A Firebase-powered point-of-sale and inventory application for small retail stores. It brings cashier operations, stock control, customer credit, expenses, receipts, user management, and business reporting into one responsive interface.

## Features

- Point-of-sale checkout and transaction recording
- Product, category, and inventory management
- Stock-in history and low-stock monitoring
- Packaging and base-unit conversion support
- Order management and edit locking
- Customer credit ledger and payment tracking
- Expense recording
- Sales summaries, product breakdowns, and transaction reports
- Receipt output and ESC/POS utilities
- Superadmin, admin, and cashier roles
- Firebase Authentication and Cloud Firestore persistence
- Light and dark themes

## Tech stack

- React 19
- Vite
- Bootstrap and Bootstrap Icons
- Firebase Authentication
- Cloud Firestore

## Local development

### 1. Install dependencies

```bash
git clone https://github.com/CoffeeDev-Err/POS-Systemv2.git
cd POS-Systemv2
npm install
```

### 2. Configure Firebase

Create a Firebase project, enable Email/Password Authentication and Cloud Firestore, then create a `.env` file in the repository root:

```env
VITE_FIREBASE_API_KEY=your-api-key
VITE_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your-project-id
VITE_FIREBASE_STORAGE_BUCKET=your-project.firebasestorage.app
VITE_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
VITE_FIREBASE_APP_ID=your-app-id
```

### 3. Start the application

```bash
npm run dev
```

## Optional demo data

The seed script can create sample users, products, categories, and store settings.

1. Download a Firebase Admin service-account key.
2. Save it as `serviceAccountKey.json` in the repository root.
3. Run:

   ```bash
   npm run seed
   ```

The seeded accounts are for local testing only. Change or remove them before deployment.

## Available commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Create a production build |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run ESLint |
| `npm run seed` | Seed Firebase with demo data |

## Deployment

Run `npm run build` and deploy the generated `dist/` directory to a static hosting platform. Add the Firebase variables to the hosting provider's environment settings.

## Security

Never commit `.env`, `serviceAccountKey.json`, or production credentials. Review Firebase Authentication and Firestore security rules before making the application public.

