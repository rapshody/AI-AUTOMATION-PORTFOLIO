# Project 4: AI Content Repurposer

**Role:** AI Automation Specialist  
**Timeline:** Built in under 4 hours  
**Status:** Complete & Production-Ready

---

## 🎯 The Problem

Content creators spend **3–5 hours per week** repurposing a single piece of content (YouTube video, blog post, podcast) into multiple platform-specific formats:
- A LinkedIn post
- A Twitter/X thread
- A newsletter blurb

This is repetitive, time-consuming work that most creators do manually — or skip entirely.

## 💡 The Solution

An AI-powered content engine that automatically:
1. **Monitors** a content source (RSS feed) for new posts.
2. **Analyzes** the content with Google Gemini AI.
3. **Generates** platform-specific content in one pass.
4. **Logs** every draft in a Google Sheet for review.
5. **Notifies** the creator via email when a new draft is ready.

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Make.com** | Automation engine |
| **Reddit RSS** | Content source |
| **Google Gemini AI** | Content generation |
| **JSON Parser** | Structure AI output |
| **Google Sheets** | Review dashboard |
| **Brevo** | Email notifications |

## 🔄 Workflow Architecture

## 📊 Sample Output

| Field | Example |
|---|---|
| **Title** | "How to make money with 500 IG posts" |
| **Summary** | A detailed breakdown of a creator who monetized 500 Instagram posts... |
| **LinkedIn_Post** | "Most creators post 500 times and get nothing. Here's the framework..." |
| **Twitter_Thread** | "1/5 Most creators waste 500 posts. Here's how one creator turned..." |
| **Newsletter_Blurb** | "This week: a creator's 500-post monetization playbook..." |

## 🚧 Challenges & Solutions

### Challenge 1: YouTube RSS Feeds Blocked
YouTube's RSS feeds are geo-restricted in Nigeria and returned `404` errors despite correct Channel IDs.

**Solution:** Pivoted to Reddit RSS feeds, which are 100% reliable and rich in text content.

### Challenge 2: Gemini Rate Limits (429 Error)
Repeated testing hit Google's free-tier quota of 20 requests per minute.

**Solution:** Implemented a "wait 60 seconds and retry" strategy and reduced test frequency.

### Challenge 3: JSON Parsing with Structured Output
Make.com's Gemini module returned structured output that needed to be broken into individual fields.

**Solution:** Created a manual `ContentJSON` data structure with 4 fields and mapped the raw `Result` pill.

## 🚀 Future Enhancements (V2.0)

- **Auto-posting to LinkedIn:** Add a second workflow that watches for `Status = Approved`.
- **Multi-platform posting:** Twitter/X, Facebook, Medium.
- **Image generation:** Use DALL·E or Stability AI to create graphics.
- **Analytics tracking:** Log engagement metrics back to the sheet.

## 🏆 Portfolio Value

This project demonstrates:
- **RSS/Webhook integration** with external content sources
- **LLM prompt engineering** for structured content generation
- **JSON parsing** and data transformation
- **Multi-system orchestration** (RSS → AI → Sheets → Email)
- **Pivot decisions** under technical constraints (YouTube → Reddit)
- **Rate limit handling** and error resilience

---

**Contact:** asuquopatrick54@gmail.com  
**Location:** Nigeria  
**Availability:** Open to freelance and full-time automation roles.
