# Sentry Setup Guide

**Issue Reference**: #2

## 1. Create Account
1. Go to [sentry.io/signup](https://sentry.io/signup/).
2. Create an account (using GitHub is recommended).
3. Create a new **Organization** (e.g., `nordwacht`).

## 2. Create Project
1. Navigate to **Projects** > **Create Project**.
2. Select Platform: **React**.
3. Set Alert Defaults: "Alert me on every error".
4. Project Name: `cybersecurity-nordwacht`.
5. Click **Create Project**.
6. **Copy the DSN** key provided (starts with `https://`).

## 3. Installation
Install the Sentry React SDK:
```bash
npm install @sentry/react
```

## 4. Configuration
### A. Environment Variables
Add your DSN to `.env`:
```env
VITE_SENTRY_DSN=your_dsn_from_step_2
```

### B. Initialize Sentry
Update your entry file (e.g., `src/main.tsx` or `src/index.tsx`) to initialize Sentry **before** rendering the app:

```tsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import * as Sentry from '@sentry/react';
import App from './App';

Sentry.init({
  dsn: import.meta.env.VITE_SENTRY_DSN,
  integrations: [
    Sentry.browserTracingIntegration(),
    Sentry.replayIntegration(),
  ],
  // Performance Monitoring
  tracesSampleRate: 1.0,
  // Session Replay
  replaysSessionSampleRate: 0.1,
  replaysOnErrorSampleRate: 1.0,
});
```
