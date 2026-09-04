# 🎙️ Voice Notes

A dead-simple voice-to-text note taker for your phone. Tap the mic, talk, and
get cleaned-up text you can copy or share into anything — messages, email,
docs, Slack, wherever.

Everything runs **on your phone**. No account, no server, no internet needed
after the page loads. Your notes never leave your device.

---

## What it does

- **🎤 Record** — one big button. Tap to start, tap to stop. It keeps
  listening through natural pauses.
- **✨ Cleans up as you talk** — capitalizes sentences, fixes `i` → `I`,
  removes filler words (*um, uh, like, you know, basically…*), tidies spacing,
  and adds periods so the text reads like writing, not a transcript.
- **🗣️ Spoken formatting commands** — say these out loud and it inserts the
  real formatting:
  | Say | You get |
  |-----|---------|
  | "new line" | line break |
  | "new paragraph" | blank line |
  | "new bullet" | `- ` bullet point |
  | "period" / "full stop" | `.` |
  | "comma" | `,` |
  | "question mark" | `?` |
  | "exclamation mark" | `!` |
  | "colon" | `:` |
- **📋 Copy** — one tap to the clipboard.
- **↗ Share** — opens Android's share sheet to send the note into any app.
- **🗑 Clear** — wipes the current note (asks first).
- **💾 Auto-saves** — your note survives closing the app. The note area is
  also editable by hand if you want to fix a word.

---

## Get it on your Android phone

The app needs to load over `https://` (Android blocks microphone access on
plain files). The free way to do that is **GitHub Pages**.

### 1. Put it on GitHub Pages
1. Sign in at [github.com](https://github.com) (free account).
2. **New repository** → name it `voice-notes` → **Public** → check
   "Add a README file" → **Create repository**.
3. **Add file → Upload files** → drag `index.html` in → **Commit changes**.
4. **Settings → Pages** → Source: *Deploy from a branch*, Branch: `main`,
   folder: `/ (root)` → **Save**.
5. Wait ~1 minute, refresh. You'll see:
   `Your site is live at https://YOUR-USERNAME.github.io/voice-notes/`

### 2. Install it as an app
1. Open that link in **Chrome** on your Android.
2. Tap the **⋮** menu → **Add to Home screen**.
3. Open it from the icon, tap the mic, and **Allow** microphone when asked
   (it only asks once, because the page is https).

---

## Notes & limits

- **Use Chrome on Android.** Voice input uses the browser's built-in speech
  engine, which is best supported in Chrome. It won't work in every browser.
- **Speech recognition needs internet** on Android (Chrome sends audio to
  Google's speech service). The *cleanup* is on-device; the *listening* is not.
- The cleanup is **rule-based**, not AI. It fixes grammar and formatting but
  does not rewrite or summarize. See below.

---

## Coming later: AI-polished notes (optional)

The current version tidies your words. A future version could **rewrite**
rambling speech into crisp bullet points or a short summary using an AI model.

That needs a small backend (a serverless function holding an API key) — it
can't stay a single offline file. Rough cost for personal use: about **$5
upfront** to fund an API account, then **free to ~$1/month** on a cheap model,
with **$0 hosting** on a free serverless tier (Cloudflare Workers / AWS Lambda
free tier). Left out for now to keep this version free and offline.

---

## Files

- `index.html` — the entire app (HTML + CSS + JavaScript in one file).

That's it. One file. Copy it anywhere and it works.
