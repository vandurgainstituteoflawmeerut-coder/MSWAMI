# MSWAMI

**Vandurga Institute of Law, Meerut**

---

## About

Official digital portal of **Vandurga Institute of Law, Meerut**.

Features:
- Modern responsive landing page
- Real authentication (Firebase Email/Password)
- Sign in, Register, Password reset
- Persistent login session

## Live App

**https://vandurgainstituteoflawmeerut-coder.github.io/MSWAMI/**

### Enable GitHub Pages (if not done yet)

1. Repository → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / Folder: **/ (root)**
4. Save

---

## 🔐 Setup Real Authentication (Firebase)

Authentication is powered by **Firebase Auth**. Follow these steps once:

### 1. Create a Firebase project
1. Go to [Firebase Console](https://console.firebase.google.com)
2. Click **Add project** → name it (e.g. `mswami-portal`)
3. Disable Google Analytics if you don’t need it → Create project

### 2. Register a Web app
1. On the project overview, click the **Web** icon (`</>`)
2. App nickname: `MSWAMI`
3. Copy the `firebaseConfig` object that appears

### 3. Enable Email/Password sign-in
1. Left sidebar → **Build** → **Authentication**
2. Click **Get started**
3. **Sign-in method** tab → **Email/Password** → Enable → Save

### 4. Add your config to the app
1. Open `index.html` in this repo
2. Find the `firebaseConfig` object (near the bottom, inside the `<script type="module">`)
3. Replace the placeholder values with your real keys:

```js
const firebaseConfig = {
  apiKey: "AIza...",              // from Firebase
  authDomain: "your-id.firebaseapp.com",
  projectId: "your-id",
  storageBucket: "your-id.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc..."
};
```

4. Commit and push the change (or edit via GitHub web UI)

### 5. (Recommended) Restrict API key
In Google Cloud Console → APIs & Services → Credentials → your Browser key:
- Add HTTP referrer restriction: `https://vandurgainstituteoflawmeerut-coder.github.io/*`

---

## What users can do

| Action | How |
|--------|-----|
| **Sign In** | Login button → enter email + password |
| **Register** | Switch to Register tab → create account |
| **Reset password** | Enter email → click Forgot password |
| **Stay logged in** | Check “Remember me” |
| **Logout** | Logout button in navbar |

---

## Repository Status

- [x] README
- [x] Landing page
- [x] Login / Register UI
- [x] Firebase Auth integration
- [ ] Firebase config filled (you need to do this)
- [ ] GitHub Pages enabled

## Contributing

Open an issue or pull request.

## Contact

Vandurga Institute of Law, Meerut

---

© 2026 Vandurga Institute of Law, Meerut. All rights reserved.
