# redline-by-harshsachora
# Redline — AI Text Editor

An AI-powered writing tool with an editorial identity: paste text, pick an edit (summarize, simplify, make professional, bullet points, fix grammar, or expand), and watch a "red pen" scanning animation mark it up before revealing the result.

## ⚠️ About the live demo
This app calls the Claude API directly from the browser. That works in Anthropic's own development environment (where I built it), but **cannot run standalone once deployed**, because a real AI API key can never be safely exposed in client-side code — anyone could open developer tools and steal it.

To make this fully live on the web, the frontend needs to talk to a small backend server that holds the API key secretly, instead of calling the AI API directly. That backend is my next build for this project — see the Roadmap section below.

For now, this repo shows the complete frontend, the UI/UX design, and the prompt logic for each editing mode.

## Features
- Six editing modes: Summarize, Simplify, Make Professional, Bullet Points, Fix Grammar, Expand
- Live word count on the input
- Animated "scan" effect during processing, styled like a manual edit pass
- One-click copy of the result
- Clear, non-technical error handling
- Fully responsive layout

## Built With
- HTML, CSS, JavaScript (vanilla — no frameworks or libraries)
- Anthropic's Claude API for the text transformations

## What I Learned
- Structuring prompts for distinct, reliable transformation tasks
- Handling async API calls, loading states, and graceful failure in the UI
- Why client-side code can never safely hold a secret API key
- Designing an interface around an AI feature instead of a generic chatbot layout

## Roadmap
- [ ] Add a small backend (serverless function) to hold the API key securely
- [ ] Connect the frontend to that backend instead of calling the AI API directly
- [ ] Deploy a fully working live version

## Run It Locally
1. Clone this repository
2. Open `redline.html` in any browser
3. Note: the AI features will not respond without a backend in place (see above)

## Author
Built by Harshvardhan Sachora as part of a growing portfolio of independent projects.
