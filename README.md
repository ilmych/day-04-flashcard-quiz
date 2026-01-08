# AI Flashcard Quiz

> Paste any text, get instant flashcards powered by Gemini AI.

Built as part of [30 Days of Vibe Code](../README.md).

## What it does

Studying is easier when you can quiz yourself. But making flashcards is tedious. This tool takes any text—notes, articles, book chapters—and uses AI to generate question-answer pairs automatically.

Paste your content, click generate, flip through flashcards, track your score.

## Demo

![Flashcard Quiz Screenshot](content/screenshot.png)

## Try it

**Live**: https://ilmych.github.io/day-04-flashcard-quiz/

You'll need a Gemini API key (free tier works): https://aistudio.google.com/apikey

## How I built it

- **Time**: ~1 hour
- **Stack**: Vanilla HTML/CSS/JS, Gemini API
- **AI assist**: Claude Code

### The Process

1. Discussed the concept—AI-powered flashcard generation
2. Built the UI with a text input area and card display
3. Integrated Gemini API for Q&A extraction
4. Added 3D flip animation for cards
5. Implemented quiz mode with scoring
6. Added keyboard shortcuts for power users
7. Tested with various content types (notes, articles, etc.)

### Prompts Used

- "what's day 4" (Flashcard Quiz was on the roadmap)
- "yes, let's build it!"
- "ooh i like it! great design job! i like this a lot. do we need to add anything else to this?"
- "yes let's publish it"

### The Gemini Prompt

```
Extract 5-10 key facts, concepts, or important points from this text.
For each one, create a flashcard with:
- A clear, specific question
- A concise answer (1-2 sentences max)

Return as JSON array: [{"question": "...", "answer": "..."}, ...]
```

## What I learned

**BYOK (Bring Your Own Key)** is a great pattern for free tools:
- No backend infrastructure needed
- No API rate limiting to manage
- No costs to scale
- Users have full control over their data

The tradeoff is UX friction (asking for a key), but for a free tool, it's worth it.

**3D CSS transforms** are surprisingly easy. The flip animation is just:
```css
.card { transform-style: preserve-3d; transition: transform 0.6s; }
.card.flipped { transform: rotateY(180deg); }
.card .back { transform: rotateY(180deg); }
```

## Features

| Feature | Description |
|---------|-------------|
| AI Generation | Gemini extracts Q&A pairs from any text |
| 3D Flip | Satisfying card flip animation |
| Quiz Mode | Track correct/incorrect answers |
| Keyboard Shortcuts | Space, arrows, S, R |
| Progress Bar | See how far through the deck |
| Shuffle | Randomize card order |
| Dark Mode | Easy on the eyes |

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Flip current card |
| `→` | Mark correct, next card |
| `←` | Mark wrong, next card |
| `S` | Shuffle deck |
| `R` | Restart quiz |

## Run locally

```bash
# Clone the repo
git clone https://github.com/ilmych/day-04-flashcard-quiz
cd day-04-flashcard-quiz

# Open in browser
open index.html

# You'll need a Gemini API key
# Get one at: https://aistudio.google.com/apikey
```

## File Structure

```
day-04-flashcard-quiz/
├── index.html          # Complete app (single file)
└── content/
    └── twitter-thread.md
```

## API Key Security

Your API key is stored in your browser's localStorage and never sent anywhere except directly to Google's Gemini API. The code is fully client-side—no backend, no tracking, no data collection.
