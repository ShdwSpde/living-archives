# Living Archives: ask history, get its own words back

Small, focused archives of one person's writing that you can question in plain language. The answer quotes the source, names the book and chapter, and every quotation is checked against the passages it came from before you see it.

![Asking the Ida B. Wells Living Archive about lynching statistics](assets/ida-archive.gif)

**Try them:**
- [The Ida B. Wells Living Archive](https://ida-b-wells-living-archive.vercel.app): five of her public-domain works, 1892 to 1920. Quote checking is live here.
- [The Du Bois Living Archive](https://dubois-living-archive.vercel.app): W.E.B. Du Bois's public-domain writing and the 1900 Paris data plates. Quote checking is built and on its way.
- [The Marcus Garvey Living Archive](https://garvey.radicalimagination.xyz/sam), with the Black Star Archive: a search of Garvey's own words.

## What it does

- **Answers from the source, not from the internet.** Each question searches only that archive's texts. The model writes from what it retrieved.
- **Quotes are checked, not trusted.** A verifier compares every quotation in the answer to the retrieved passages and marks it verified or not. OCR quirks in old scans are allowed for; a changed word is caught.
- **Real chapters.** Book chapters are read from each book's own contents page, so a citation points somewhere a reader can open.
- **Honest about gaps.** When the archive has no word for a modern term, it says so instead of guessing.

## Why

We tested our own archives with 54 questions of the kind real visitors ask: slang, words whose meaning changed, ideas a figure practiced but never named. The early versions failed in specific ways, including quoting other writers as if they were the subject. The fixes above came out of those failures. The lesson: the archive has to stay human-checked, and the software has to show its work.

## How it's built

Retrieval over vector search (pgvector or Firestore, depending on the archive), embeddings, a streamed answer, and a quote verifier with its own tests. React and Vite front ends on Vercel.

## Demo, in captions

**▶ [Watch the demo](https://radicalimagination.xyz/demos/living-archives.mp4)** (silent, captioned, under 30 seconds)

1. "Ask Ida B. Wells a question."
2. "The archive searches her own books, nothing else."
3. "It answers in her words, with the book and chapter."
4. "Every quotation is checked against the page it came from."
5. "Living Archives. Radical Imagination."

The application code lives in private repositories. This page is the public showcase.

**Radical Imagination**, a cultural technology studio in Queens. [radicalimagination.xyz](https://radicalimagination.xyz)
