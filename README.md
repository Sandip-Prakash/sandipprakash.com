# sandipprakash.com

Personal site for Sandip Prakash, built like a product launch page. Static HTML plus one Vercel serverless function for the "Ask Sandip" AI.

## Files
| Path | What it is |
|---|---|
| `index.html` | The whole site (HTML, CSS, JS in one file) |
| `knowledge/sandip.md` | Everything the AI knows. Edit this to make the AI smarter. |
| `api/ask.js` | Serverless function: sends questions + the knowledge file to Claude, streams the answer |
| `vercel.json` | Bundles the knowledge file with the function |
| `assets/` | Avatar, portrait and share image crops |
| `resume.pdf`, `pfp.*` | Resume and original photo |

## Setup on Vercel
Settings → Environment Variables:
- `ANTHROPIC_API_KEY` (required). Enable it for **Production** and **Preview**.
- `ANTHROPIC_MODEL` (optional). Defaults to `claude-haiku-5-5`.

Redeploy after adding variables.

## Improving the AI
1. Edit `knowledge/sandip.md` and push.
2. Questions it couldn't answer appear in Vercel → Logs as `"type":"knowledge_gap"`. Add those answers to the file.

The repo is public, so never put a phone number, salary or anything confidential in the knowledge file.

## Previewing changes
Push to any branch other than `main` and Vercel builds a preview URL. Merge to `main` to go live.
