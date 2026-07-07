# Troubleshooting

Find your symptom below. Each one has the real cause and the exact fix. If your issue is not here, tell Claude exactly what you see on your screen and it will help.

---

## Plan and connector limits

### "Add custom connector" is missing, greyed out, or it will not add the second or third tool
**Cause:** You are on Claude Free, which allows only one custom connector. The Solnest Cinematic Director needs three.
**Fix:** Upgrade to **Claude Pro or Max.** There is no workaround on the free plan. This is the most common blocker of all, so check it first.

### I am on Pro or Max but still only see one connector slot
**Fix:** Make sure you are signed in to the right account in the desktop app (the one with the paid plan). Sign out and back in if needed. Then reopen Customize, then Connectors.

---

## The Solnest Cinematic Director skill

### The skill will not upload, or it uploads and then does nothing
**Cause 1:** Code execution is off. Skills need it.
**Fix:** Go to Settings, then Capabilities, and turn **Code execution** on. Then upload the skill again.

**Cause 2:** You are on the free plan. Uploading skills is supported on all plans now, but if it refuses, confirm your plan and that you are signed in.

**Cause 3:** The wrong file was chosen. You must upload the **`solnest-cinematic-director.zip`** from the `skill` folder in this kit, not the `.skill` file and not a loose `SKILL.md`.

### I do not see the Solnest Cinematic Director in my Skills list
**Fix:** Reopen Customize, then Skills, and check the list. Make sure the toggle next to the Solnest Cinematic Director is **on.** If it is not there at all, upload the zip again.

### I dragged the skill zip into the chat and nothing happened
**Cause:** The skill is not installed by dragging it into a chat. It is uploaded in the Skills area.
**Fix:** Go to Customize, then Skills, then plus, then Create skill, then Upload a skill, and choose the zip.

### The director did not start when I asked for a video
**Fix:** Make sure the Solnest Cinematic Director skill toggle is on. Then ask in a way that triggers it, for example "make me a Solnest video for this listing" and paste the link. Naming the video directly helps.

---

## Firecrawl will not connect

### It errors when added, or scraping returns nothing
**Cause 1:** The link is wrong. It must end in `/v2/mcp` and your `fc-` key must be inside the link.
**Fix:** Use exactly `https://mcp.firecrawl.dev/YOUR-FIRECRAWL-KEY/v2/mcp` with your real key swapped in.

**Cause 2:** Something was typed in the OAuth boxes.
**Fix:** Leave OAuth Client ID and Secret blank. The key is already in the link.

**Cause 3:** The key is wrong or expired.
**Fix:** Get a fresh key at firecrawl.dev/app/api-keys and rebuild the connector.

### The listing photos did not all come through
**Cause:** Listing galleries load slowly, so a quick read can miss some.
**Fix:** This is normal. The director waits longer on purpose and trusts the room labels. If a room is missing, it will substitute the next best shot and tell you which one it swapped so you can fix it later.

---

## Higgsfield will not connect

### Cannot read the balance, or it errors when added
**Cause 1:** The sign-in did not finish.
**Fix:** Remove the connector and add it again. When the browser window opens, complete the Higgsfield login fully and approve access.

**Cause 2:** The link was rejected.
**Fix:** Try the link without the ending: `https://mcp.higgsfield.ai`.

### "MCP server connection lost" while importing or generating
**Cause:** This is a known, usually temporary Higgsfield hiccup, often when importing an outside image link.
**Fix:** Just retry. It normally goes through on a second or third try. If it stays down across several tries, Higgsfield itself may be having a moment. Wait a bit and try again later.

### A clip failed or came back flagged
**Cause:** Sometimes a prompt trips a content filter.
**Fix:** The director will retry with a softer prompt. If one specific photo keeps failing, swap in a different photo for that beat.

### I ran out of credits partway
**Fix:** Top up a small credit pack at higgsfield.ai. Each video needs roughly 30 to 40 credits, double that if you asked for both video shapes.

---

## Descript will not connect

### It errors when added, or read commands fail
**Cause 1:** The sign-in did not finish.
**Fix:** Remove the connector and add it again, and complete the Descript login fully in the browser window.

**Cause 2:** Plan access. On some plans the connection may be limited.
**Fix:** Confirm you are on the **Hobbyist plan or higher.** This is also what you need for a clean video, so it is worth doing regardless.

### My finished video has a watermark or looks low quality
**Cause:** You are on the free Descript plan, which watermarks output and caps it at 720p.
**Fix:** Upgrade Descript to **Hobbyist or higher** for clean, watermark-free 1080p.

### The job failed partway through stitching
**Cause:** You ran out of Descript media minutes or AI credits.
**Fix:** Check both in your Descript account. Free up minutes or upgrade your plan, then run it again.

### The download link does not work anymore
**Cause:** The direct download link expires after a while.
**Fix:** Use the share link to watch it, or open the Descript project link and export again. Save the file soon after it is made next time.

---

## General

### A tool says it is connected but Claude cannot use it in the chat
**Fix:** In the message box, click the plus, find the connector, and toggle it on for this chat. If that does not do it, start a brand-new chat, drag this kit in again, and tell Claude which tools are already connected so it picks up where you left off.

### Do I need to restart the app after connecting something?
**Usually no.** Connectors and skills become available right away. If a just-added tool does not show up, restarting the app or starting a new chat clears it up.

### The director stopped after the clips and did not make the final video
**Cause:** Descript is not connected.
**Fix:** Connect Descript (Step 5 in the setup guide). The director will hand you the five raw clips in the meantime, and can stitch them once Descript is on.

### I want to start completely over
**Fix:** You can remove any connector under Customize, then Connectors, and remove the skill under Customize, then Skills, then add them back. Nothing you do here is permanent or breakable.
