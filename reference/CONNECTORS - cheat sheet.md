# Connectors Cheat Sheet

A one-page reference for the four tools the Solnest Cinematic Director uses. Claude pulls from this during setup, and you can keep it for later.

All four are added inside the Claude app under **Customize, then Connectors** (older builds call the menu **Settings**). Three of them use **Add custom connector** and a web link. Google Drive is built in.

---

## Quick table

| Tool | What it does for the director | How to add it | The link to paste | Login |
|---|---|---|---|---|
| **Firecrawl** | Reads the listing page and pulls the photos | Add custom connector | `https://mcp.firecrawl.dev/YOUR-FIRECRAWL-KEY/v2/mcp` | Key is in the link, no separate login |
| **Higgsfield** | Generates the five cinematic video clips | Add custom connector | `https://mcp.higgsfield.ai/mcp` | Sign in to Higgsfield in the browser popup |
| **Descript** | Stitches the clips into one video with music | Add custom connector | `https://api.descript.com/v2/mcp` | Sign in to Descript in the browser popup |
| **Google Drive** | Optional. Saves the finished video to a folder | Built-in connector, click Connect | Not needed | Sign in to Google in the browser popup |

---

## Firecrawl details

- **Get your key:** sign in at firecrawl.dev, then open **firecrawl.dev/app/api-keys** and copy the key. It starts with `fc-`.
- **The free plan is fine** for making videos from single listings.
- **Paste the full link** with your key dropped in where it says YOUR-FIRECRAWL-KEY. Example: `https://mcp.firecrawl.dev/fc-abc123.../v2/mcp`.
- **Leave the OAuth boxes blank.** The key lives in the link.
- **Must end in `/v2/mcp`.** Not v1, not without it.
- **Do not** paste this link into any config file. It goes in the Add custom connector box only.

## Higgsfield details

- **No key to copy.** You paste the link, then sign in to your Higgsfield account in the popup.
- **Credits:** each video uses roughly 30 to 40 credits across the five clips. A small credit pack covers several videos. Check your balance at higgsfield.ai or just ask Claude to read it after connecting.
- **If the link is rejected,** try it without the ending: `https://mcp.higgsfield.ai`.
- Free Higgsfield output is watermarked, so a small paid credit pack is worth it.

## Descript details

- **No key to copy.** You paste the link, then sign in to your Descript account in the popup.
- **Plan matters:** for a clean, watermark-free 1080p video you need the **Hobbyist plan or higher.** The free plan watermarks the video and caps it at 720p.
- Two things can run out mid-job and cause a failure: your Descript **media minutes** and your **AI credits.** If a job fails partway, check both.
- The direct **download link expires,** so save the finished file soon after it is ready. The share link to watch stays live.

## Google Drive details

- Built in, so it is the easiest. No link to paste.
- Find Google Drive in the Connectors list and click **Connect**, then sign in to Google.
- This one does not count against your connector limit.

---

## The plan rule that catches everyone

Claude **Free allows only one custom connector.** The Solnest Cinematic Director needs three custom connectors (Firecrawl, Higgsfield, Descript). So you must be on **Claude Pro or Max.** Google Drive is built in and does not count, but the three custom ones do. If "Add custom connector" is missing or greyed out, or it refuses to add the second or third one, this is almost always why.
