# Chat with My Background

An AI-powered page that lets anyone ask questions about my experience, projects, and skills — and get answers grounded in my actual background.

## What it does

Opens a chat interface where the hiring manager (or anyone) can ask natural questions like:

- "What did she build at Amazon?"
- "Tell me about the Equatic pipeline"
- "Why does she want to work at Shopify?"
- "What are her strongest technical skills?"

The AI answers in first person, only drawing from my real background. It will not make things up.

## How it works

A single HTML file. No framework, no build step, no dependencies to install.

It calls the [Anthropic Messages API](https://docs.anthropic.com/en/api/messages) with a system prompt loaded with my resume. The API key is handled by the Anthropic platform when viewed through Claude.ai artifacts — to run it locally you would need to add your own key.

## Run it locally

If you want to run this on your own machine with your own Anthropic API key, add this just before the closing `</body>` tag or modify the fetch headers in the script:

```js
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_KEY_HERE',
  'anthropic-version': '2023-06-01'
}
```

Then open `index.html` directly in a browser. No server needed.

## Adapt it for yourself

To use this as your own resume chat:

1. Replace the `SYSTEM` prompt in `index.html` with your own background
2. Update the header name and initials
3. Swap out the suggested question chips for topics relevant to your experience
4. Deploy to GitHub Pages or any static host

## Stack

- Plain HTML, CSS, JavaScript
- Anthropic Claude API (claude-sonnet-4-20250514)
- No build tools, no npm, no framework
