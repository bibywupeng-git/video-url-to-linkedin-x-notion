# Turn TikTok Video URLs into LinkedIn Drafts & X Threads (Notion + Make + Apify + OpenAI)

Turn any TikTok video URL into:
- ✅ a ready-to-post **LinkedIn draft**
- ✅ a full **X (Twitter) thread**
…and save everything back to **Notion** for easy review & publishing.

**Make template:** https://us2.make.com/templates/18386-turn-video-urls-into-linkedin-posts-x-threads-notion-apify-openai

> **Currently supported:** TikTok video URLs  
> **Coming next (if users need it):** Instagram / YouTube / more video platforms

---

## Quick Demo

### GIF Preview
![Demo](./template_demo.gif)

### Video Demo
> GitHub can preview MP4 files on the file page.  
> Open: `demo_video.mp4` in this repo to watch the full demo.

---

## Who is this for?

If you regularly collect videos and need to turn them into posts, this saves time every day:
- Content creators & social media managers
- Founders / marketers who repurpose content
- Knowledge workers who capture ideas in Notion
- Agencies doing multi-channel content ops

---

## What it does (in plain English)

1) You paste a **TikTok URL** into a Notion table and set **Status = NEW**  
2) Run the Make scenario (or schedule it)  
3) The workflow fetches the **transcript** (internal step), then uses OpenAI to generate:
   - a **LinkedIn draft**
   - an **X thread**
4) The results are saved back to your Notion row, and the status becomes **DONE**  
5) You review and publish when ready

> Note: The **clean transcript is an internal processing step** and is **not written back to Notion** by this template.

---

## Outputs saved to Notion

Each processed row will have:
- **LinkedIn Draft** (ready to copy/paste)
- **X Thread** (7–10 tweets format, ready to post)
- **Status** (NEW → PROCESSING → DONE / ERROR)
- **Error message** (only if something fails)

---

## Requirements

You’ll need:
- A **Make.com** account
- A **Notion** workspace + integration connection in Make
- An **Apify** account (for the TikTok transcript actor)
- An **OpenAI** API key (for content generation)

---

## Notion Database Setup (Required)

Create a Notion database (Table view) with the following **properties**.

> The template expects this structure so it can run without extra edits.

### Required properties

| Property name | Type | Example / Notes |
|---|---|---|
| `Title` | Title | Optional, e.g. “Intro to GenAI (TikTok)” |
| `video_url` | URL | TikTok video link |
| `status` | Select | Must include: `NEW`, `PROCESSING`, `DONE`, `ERROR` |
| `linkedin_draft` | Text (or Rich text) | Output field |
| `x_thread` | Text (or Rich text) | Output field |
| `error_message` | Text (or Rich text) | Filled when error happens |

### Optional (recommended) properties

| Property name | Type | Why it helps |
|---|---|---|
| `Source` | Select | e.g. TikTok / Instagram (future) |
| `Author` | Text | Store creator name/handle if you want |
| `Topic` | Multi-select | Organize your content library |
| `Created time` | Created time | Useful for sorting & tracking |

**Important:**  
- Your `status` select options must match **exact spelling** used in the scenario (NEW/PROCESSING/DONE/ERROR).

---

## How to use

### 1) Import the Make template
Open the template link and create your own scenario:
https://us2.make.com/templates/18386-turn-video-urls-into-linkedin-posts-x-threads-notion-apify-openai

### 2) Connect accounts (one-time)
- Notion connection
- Apify connection
- OpenAI API key

### 3) Point the scenario to your Notion database
Select your database as the data source.

### 4) Run it
- Add a row in Notion with:
  - `video_url` = your TikTok link
  - `status` = `NEW`
- Run scenario (manual “Run once”) or enable scheduling
- Wait for status to become `DONE`
- Copy the generated drafts and publish

---

## Customization ideas

You can easily tailor the outputs:
- Change tone (professional / casual / founder voice)
- Add your brand style guide / forbidden words
- Set tweet count (7–10) and character limits
- Add a “hook library” or CTA patterns
- Save extra outputs (summary, key takeaways, hashtags)


---

## FAQ

### Does this post automatically to LinkedIn or X?
No — it generates drafts and saves them to Notion. You review and publish.

### Do I need subtitles or voiceover in the demo video?
Not required. Subtitles help a bit, but a short clean demo is usually enough.

### What about other platforms?
This version supports **TikTok URLs**. If you need Instagram / YouTube next, we’ll extend the workflow.

---

## Troubleshooting

- If `status` becomes `ERROR`, check `Error Message` in Notion.
- Verify the TikTok URL is reachable and public.
- Confirm your Apify/OpenAI credentials are valid.
- If your Notion properties don’t match, remap them in Make.

---

## Credits

Built with:
- Make.com
- Notion
- Apify (TikTok transcript actor)
- OpenAI

If you try it and it saves your time, tell me what platform you want next (Instagram / YouTube / others) and what output format you prefer.
