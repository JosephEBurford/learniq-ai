# LearnIQ — Build 04B (live AI)

Walmart-inspired fictional workforce learning portfolio prototype. Not an official Walmart product. Training records and associates are sample data.

## Deploy to Vercel

1. Upload `index.html`, `package.json`, `.gitignore`, and the `api/copilot.js` file to the GitHub repository. Preserve the `api` folder.
2. In Vercel project → Settings → Environment Variables, add `OPENAI_API_KEY` with your own API key. Select Production (and Preview if needed). **Never commit this key to GitHub or paste it into HTML.**
3. Optionally add `OPENAI_MODEL` (default: `gpt-4o-mini`).
4. Redeploy the project (Deployments → latest → Redeploy), or push a new GitHub commit after adding the variable.
5. Open the site and ask Copilot a free-text question. The API route is `/api/copilot`.

## Notes

- AI requests are sent through a Vercel serverless function, not directly from the browser to OpenAI.
- The browser sends **fictional** training data for demo grounding; it is not an authenticated data service.
- Assignments still require explicit manager approval and are saved locally in the browser.
- The API key owner is responsible for API usage costs. For a public portfolio, add authentication/rate limiting or disable the endpoint when not demonstrating it.
- A public endpoint without authentication may be abused. This prototype is not production-ready for real employee data.
