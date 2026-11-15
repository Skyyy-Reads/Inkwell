# Inkwell on GitHub Pages

`index.html` is the whole app. It needs a free Firebase project for shared storage.

1. **Firebase:** console.firebase.google.com > Add project (free Spark plan is enough).
2. **Web app config:** Project settings > Your apps > Web (</>) > register, copy the `firebaseConfig` values into `FIREBASE_CONFIG` near the top of `index.html`.
3. **Sign-in:** Build > Authentication > Get started > Sign-in method > enable **Anonymous**. (No Google account needed. People just type a display name.)
4. **Database:** Build > Firestore Database > Create (production mode). Open Rules, paste `firestore.rules`, Publish.
5. **GitHub:** push `index.html` to a repo, then Settings > Pages > Deploy from branch (main, / root). Open `https://YOUR-USERNAME.github.io/REPO/` and share it with your co-author.

Notes:
- Each browser is its own identity. Clearing site data or switching device means a new anonymous user with a new name prompt.
- Anyone who has your site's link can open it and write, so keep the link private. Private notes are still only readable by their own browser identity.
- File attachments are off in this build (Firebase Storage needs a paid plan).
