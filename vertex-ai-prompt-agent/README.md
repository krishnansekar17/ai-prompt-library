# 🔷 Vertex AI Prompt Agent — Prompts

This folder contains prompts discovered and refined using **Google's Vertex AI Prompt Agent** inside Vertex AI Studio.

The Prompt Agent takes your raw task description written in plain language and converts it into a structured, optimized prompt ready for any GenAI tool or LLM.

---

## 📄 Prompts in This Folder

| File | Use Case | Platform |
|------|----------|----------|
| [`shopify-blog-html-optimizer.txt`](./shopify-blog-html-optimizer.txt) | Convert raw blog article → fully optimized HTML for blog platforms | Shopify, WordPress, any CMS |

---

## 🛍️ Prompt 1: Shopify Blog HTML Optimizer

### What It Does

Takes a raw blog article (plain text or document) and converts it into a **fully structured, semantic HTML snippet** ready to paste directly into any blog editor — Shopify, WordPress, or a custom CMS.

The output HTML is optimized for:
- **SEO** (Search Engine Optimization) — proper heading structure, semantic tags, internal linking
- **AEO** (Answer Engine Optimization) — structured content that AI answer engines can extract cleanly
- **GEO** (Generative Engine Optimization) — content formatted for visibility in AI-generated summaries and responses

### What You Get in the Output

- Clean semantic HTML (no `<html>`, `<head>`, or `<body>` wrapper tags needed)
- `<h2>`, `<h3>` heading structure for proper content hierarchy
- Internal links pulled from your sitemap URLs (contextually placed, not stuffed)
- Image placeholders with pre-written descriptive `alt` text for accessibility and SEO
- JSON-LD schema markup where relevant (for products, people, concepts)
- No unnecessary inline CSS or JavaScript bloat

### How to Use This Prompt

**Step 1:** Go to [Vertex AI Studio](https://console.cloud.google.com/vertex-ai/studio) and open **Chat** or **Prompt Agent**

**Step 2:** Copy the full contents of [`shopify-blog-html-optimizer.txt`](./shopify-blog-html-optimizer.txt)

**Step 3:** Paste the prompt into the input field

**Step 4:** Replace the two placeholders:
- After `**Blog Article Content:**` — paste your raw blog article text (or upload the document)
- Replace `{sitemap_urls_list}` — add your sitemap URLs, one per line, e.g.:
  ```
  https://yourstore.com/sitemap.xml
  https://yourstore.com/sitemap_products_1.xml
  ```

**Step 5:** Run the prompt. Copy the HTML output and paste it into your blog editor's HTML/code view.

### Real-World Result

This prompt was tested on a raw SEO blog article for a Shopify fragrance store. The output included:
- Proper `<section>` and `<article>` structure
- Internal links to relevant product and collection pages from the sitemap
- Image placeholders with descriptive alt text for every key section
- JSON-LD schema for fragrance ingredients mentioned in the article

**Time saved:** What normally takes 2-3 hours of manual HTML formatting was done in under 2 minutes.

---

## 🔧 Tool Info

| Field | Detail |
|-------|--------|
| Tool | Vertex AI Prompt Agent |
| Platform | Google Cloud — Vertex AI Studio |
| Access | Free with Google Cloud account (usage-based pricing may apply) |
| URL | https://console.cloud.google.com/vertex-ai/studio |

---

## 📌 Notes

- You do not need to know HTML to use this prompt — the AI handles all the code
- Works best when the article is already written in clean, structured prose
- For best internal linking results, provide multiple sitemap URLs (products, collections, blogs)
- The prompt instructs the AI NOT to add `<h1>` — because Shopify adds that automatically from the blog post title

---

*Discovered via Google Vertex AI newsletter. Tested in real SEO workflows.*
