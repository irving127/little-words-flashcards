# Little Words: Toddler Flashcards

A simple flash card game for toddlers, built for Kobe (3) and Jayden (2).

Tap a card to hear the word. No scores in Learn mode, no failure in Find It mode, just big buttons and praise.

## What is in v1

- 24 words: animals, food, nature, and colors, expanded from the original 10-word iOS starter
- Each word in English, Mandarin (characters + pinyin), and French
- Learn mode: one big card, tap to hear it, Back / Shuffle / Next
- Find It game: "Find the Dog! 找狗!" with 3 choices, stars for a correct tap, a gentle shake and the word spoken for a wrong tap
- Speech uses the device's built-in voices (Web Speech API: en-US, zh-CN, fr-FR), slowed to 0.8x for toddlers. No backend, no account, no ads
- Language selector for parents: English + 中文 (default), English only, 中文 only, Français, English + Français

## Run it

Open `index.html` in any browser, or serve the folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000 on the same Wi-Fi, e.g. on an iPad
```

Best experience: add it to an iPad home screen and use it full screen.

## Put it on GitHub

```bash
cd toddler-flashcards
git init
git add index.html README.md
git commit -m "Little Words v1: 24 flashcards, Learn + Find It, EN/ZH/FR speech"
gh repo create little-words-flashcards --public --source=. --push
```

Then turn on GitHub Pages (repo Settings: Pages: Deploy from branch `main`, folder `/root`) for a shareable live link.

## Roadmap

- v1.1: Record a parent's voice for each word (toddlers respond better to a familiar voice than the robot voice, same note as in the iOS starter)
- v1.2: Categories screen (Animals / Food / Colors) so Kobe can pick a theme
- Later: Port back to the iOS SwiftUI version in `workspace/goals/bilingual-toddler-learning-app/files/ContentView-starter.swift` for the App Store goal (10 downloads)

## Stack

Vanilla HTML, CSS, and JavaScript in one file. No framework, no build step, on purpose: it proves the fundamentals and it will still run in 10 years.
