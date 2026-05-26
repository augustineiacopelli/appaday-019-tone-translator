# 019 · Tone Translator

Part of the [AppADay](https://augustineiacopelli.github.io) project — one complete web app shipped every day.

## What It Does

Paste any text and translate it into a different tone. Four options: **Formal** (polished, professional), **Casual** (relaxed, conversational), **Direct** (concise, no-fluff), and **Warm** (empathetic, human). Claude rewrites your text while preserving the core meaning.

## How to Use

1. Open Settings (top right) and enter your Anthropic API key and email address — both are saved locally in your browser and never sent anywhere except the Anthropic API.
2. Paste or type your text in the input box.
3. Select a tone.
4. Hit **Translate Tone** and watch the result stream in.
5. Copy to clipboard or tap **Email** to send the result to yourself or anyone else via your mail client.

## Technical Notes

- Vanilla HTML/CSS/JS — no frameworks, no build step
- Calls the Anthropic API directly from the browser using the `anthropic-dangerous-direct-browser-access: true` header
- Streams the response token-by-token via the SSE endpoint
- API key and email stored in `localStorage` — never in source
- Email sent via `mailto:` link, which opens your default mail client

## Definition of Complete

- [x] Functional — translates text via Claude with no errors
- [x] Single Purpose — one job: change the tone of text
- [x] Mobile Friendly — responsive grid, tap targets sized correctly
- [x] Visually Polished — editorial paper aesthetic, streaming output, consistent type
- [x] Published — live at augustineiacopelli.github.io/appaday-019-tone-translator
