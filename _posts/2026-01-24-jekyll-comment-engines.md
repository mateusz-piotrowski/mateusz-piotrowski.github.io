---
layout: post
title: "Jekyll comment engines"
comments: true
post_number: 17
date: 2026-01-24 00:00:00 +0100
categories: general
tags: Jekyll comment-engine
---

## Choosing the Right Comment Engine for Your Jekyll Blog

Hi all,

Today I want to share a guide about choosing the right comment engine for your Jekyll blog. Static site generators like Jekyll offer incredible performance and simplicity, but adding a robust commenting system can be challenging. This guide explores the best comment engines to enhance reader interaction while maintaining your site's core philosophy.

## Understanding Jekyll Comment Solutions

When selecting a comment system for your Jekyll blog, consider these key factors:
- **Privacy**: How the system handles user data
- **Ease of Integration**: Technical complexity of setup
- **Customization**: Moderation and styling options
- **Performance**: Impact on site load times
- **Cost**: Free vs. paid solutions

## Third-Party Hosted Comment Systems

### 1. Giscus: The GitHub-Powered Solution

- **Pros**: 
  - Privacy-friendly
  - Ad-free
  - Seamless GitHub integration
  - Lightweight and fast
- **Cons**:
  - Requires GitHub account for commenting
  - Limited to GitHub users

### 2. Disqus: The Popular Choice

- **Pros**:
  - Widely used
  - Comprehensive moderation tools
  - Easy installation
- **Cons**:
  - Displays ads in free version
  - Potential privacy concerns
  - Heavyweight compared to static alternatives

### 3. Utterances: Minimalist GitHub Comments

- **Pros**:
  - Uses GitHub Issues for comments
  - Open-source
  - No tracking or ads
- **Cons**:
  - GitHub account required
  - Limited styling options

## Static Comment Systems

### 1. Staticman: Pure Static Approach

- **Pros**:
  - Comments stored directly in your repository
  - Complete control over data
  - No external dependencies
- **Cons**:
  - Complex setup
  - Requires additional hosting (e.g., Heroku)
  - Manual moderation

### 2. Jekyll::StaticComments

- **Pros**:
  - Full control over comment storage
  - No external services
- **Cons**:
  - Extremely manual process
  - No real-time interaction

## Self-Hosted Solutions

### 1. Isso: SQLite-Powered Comments

- **Pros**:
  - Complete data ownership
  - Lightweight
  - No external tracking
- **Cons**:
  - Requires server management
  - Technical setup complexity

### 2. Commento: The Premium Feel

- **Pros**:
  - Fast and lightweight
  - Built-in spam protection (Akismet)
  - Privacy-friendly (no ads/tracking)
- **Cons**:
  - Paid service (or complex self-hosting)
  - Requires server for self-hosting

### 3. Cactus Comments: Matrix-Based Privacy

- **Pros**:
  - Federated and decentralized (Matrix protocol)
  - Extremely privacy-focused
  - Open-source
- **Cons**:
  - Requires a Matrix account for moderation
  - Interface might feel "different" to non-Matrix users

## Creative Alternatives

### 1. GitHub Discussions

- Perfect for developer-focused blogs
- Integrates naturally with technical content
- Leverages existing GitHub community

### 2. Mastodon Comments

- Decentralized social media integration
- Appeals to privacy-conscious audiences
- Promotes wider content discovery

### 3. Webmentions: The IndieWeb Standard

- **Pros**:
  - Decentralized and open standard
  - Aggregates mentions from across the web (X, Mastodon, blogs)
- **Cons**:
  - Can be tricky to set up for static sites
  - Requires a service like webmention.io

## Getting Started: Integrating Comments in Chirpy

Since this blog uses the **Jekyll Chirpy theme**, you can enable many of these systems directly in your `_config.yml`.

### Step-by-Step for Giscus (Recommended)

1. **Prepare GitHub**: Create a public repository (e.g., `blog-comments`) and enable **Discussions**.
2. **Install Giscus App**: Grant access to your repository at [giscus.app](https://giscus.app).
3. **Configure Jekyll**: Open `_config.yml` and update the `comments` section:

```yaml
comments:
  provider: giscus
  giscus:
    repo: "your-username/blog-comments"
    repo_id: "..."
    category: "Announcements"
    category_id: "..."
    # ... other settings from giscus.app
```

4. **Front Matter**: Ensure `comments: true` is set in your post's Front Matter (it's enabled by default in Chirpy).

### For Other Engines

If you choose a system not natively supported by Chirpy (like Cactus), you'll need to create a custom include in `_includes/comments.html` (if your theme allows) or modify the layout directly.

## Recommendation Matrix

| Solution | Privacy | Ease of Use | Cost | GitHub Integration |
|----------|---------|-------------|------|-------------------|
| Giscus | High | Easy | Free | Excellent |
| Utterances | High | Moderate | Free | Excellent |
| Disqus | Low | Very Easy | Freemium | None |
| Staticman | High | Complex | Free | Good |
| Commento | High | Moderate | Paid | None |
| Cactus | Very High | Moderate | Free | None |
| Webmention | High | Complex | Free | N/A |

## Final Thoughts

Choosing a comment system depends on your specific needs. For most Jekyll blogs, **Giscus** offers the best balance of privacy, ease of use, and GitHub integration. Technical blogs might prefer Utterances, while those valuing complete control could explore Staticman or self-hosted options.

**Pro Tip**: Always prioritize reader privacy and site performance when selecting a comment engine.

It is everything that I have for today.  
Everyone is a blacksmith of own fate.  
Mateusz.
