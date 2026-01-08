# Day 4 Twitter Thread

## Tweet 1 (Hook)

Day 4/30: AI Flashcard Quiz

Paste any text. Get instant flashcards. Quiz yourself.

Uses Gemini AI to generate Q&A pairs from your content. Built in ~1 hour.

## Tweet 2 (The Problem)

The problem:

You're studying something—notes, an article, a chapter. You want to quiz yourself, but making flashcards manually is tedious.

What if AI could read your content and generate the questions for you?

## Tweet 3 (The Solution)

What it does:

1. Paste any text (notes, articles, chapters)
2. AI extracts key concepts → generates Q&A pairs
3. Flip through flashcards with 3D animation
4. Quiz mode: track what you got right/wrong
5. Shuffle, restart, study again

All in the browser. No backend.

[screenshot of the flashcard UI]

## Tweet 4 (The Design)

The UX details:

- Cards flip with a satisfying 3D rotation
- Keyboard shortcuts: Space (flip), ← (wrong), → (right), S (shuffle), R (restart)
- Progress bar shows how far through the deck you are
- Score tallies correct/incorrect
- Dark mode by default (easy on the eyes)

## Tweet 5 (The AI Part)

How the AI works:

Uses Google's Gemini API (user brings their own key).

Prompt: "Extract 5-10 key facts. For each, create a question and answer. Return JSON."

The key insight: Gemini is good at structured extraction. Give it a schema, it follows it. No parsing headaches.

## Tweet 6 (What I Learned)

Lesson from today:

**BYOK (Bring Your Own Key)** is underrated for free tools.

- No backend needed
- No rate limiting to manage
- No API costs for me
- User has full control

The UX tradeoff (asking for a key) is worth it for the simplicity.

## Tweet 7 (CTA + Links)

Try it: https://ilmych.github.io/day-04-flashcard-quiz/

You'll need a Gemini API key (free tier works fine): https://aistudio.google.com/apikey

Code: https://github.com/ilmych/day-04-flashcard-quiz

Tomorrow: Deadline Dice (shake your phone to get a random deadline)

#30DaysOfVibeCode #BuildInPublic

---

# Short Version (if needed)

Day 4/30: AI Flashcard Quiz

Paste text, get instant flashcards powered by Gemini AI.

- 3D flip animations
- Quiz mode with scoring
- Keyboard shortcuts
- BYOK (bring your own API key)
- ~1 hour to build

Try it: https://ilmych.github.io/day-04-flashcard-quiz/

#30DaysOfVibeCode
