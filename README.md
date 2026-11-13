# Card Reader

A one-page web app for Heads Up-style games. You prop a phone so its back camera sees the screen showing the card. When the card changes, the phone reads the word with Claude and shows it in big text.

Everything is in `index.html`. There's no build step and no server. The API key is typed in on the phone and saved only in that phone's browser, so it's never in this repo.

## Open it

**https://rickstiles25-tech.github.io/phone-watcher/**

GitHub Pages publishes this repo's `main` branch. After you change `index.html` here, the site updates within a minute or two. The repo is public, which free accounts need for Pages. That's fine because the API key isn't in the code.

## Get an API key

1. Sign in at [console.anthropic.com](https://console.anthropic.com).
2. Add a few dollars of credit under **Billing**. The API is pay-as-you-go and separate from a Claude.ai subscription.
3. Under **API keys**, create a key and copy it (it starts with `sk-ant-`).
4. Optional: set a monthly spend limit under **Limits** so a forgotten tab can't run up a bill.

## Use it

1. Open your Pages link on the phone (Safari on iPhone, Chrome on Android).
2. Paste the key, pick a model, and tap **Start camera**. Allow camera access when asked.
3. Lean the phone on something so it's steady, aim it at the screen, and use **Zoom** until the card fills the preview.
4. The word appears when a new card settles on screen. The old word dims as soon as the card changes. **Read now** forces a read.

Tips:
- **Opus 5.5** is the most accurate on blurry or glary shots. **Haiku 5.5** answers faster and costs much less. The running cost estimate is in the bottom-right.
- If it reads too often (people walking past, lights flickering), lower **Sensitivity** in Settings. If it misses card changes, raise it.
- If the screen keeps locking on an iPhone, set **Settings → Display & Brightness → Auto-Lock** to *Never* while you play.
- It automatically pauses for 15 seconds if it's reading more than 30 times a minute, which usually means the phone is moving.
