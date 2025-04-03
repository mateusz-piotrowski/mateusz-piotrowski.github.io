---
layout: post
title: "Jekyll theme replacement"
comments: true
post_number: 15
date: 2025-04-03 00:00:00 +0100
categories: general
tags: jekyll minima chirpy
---

## Migrating My Blog from Minima to Chirpy Theme

Hi all,

Today I want to share an exciting update about my blogging journey. After some consideration, I decided to revamp my Jekyll-powered blog by switching from the minimalist **Minima theme** to the feature-rich and sleek **Chirpy theme**. In this post, I'll share my migration experience, highlight key differences through a comparative table, and outline some exciting features introduced by **Chirpy**.

### Migration Process

Switching themes in Jekyll generally involves updating configuration files and managing dependencies. Here are the essential steps I followed:

1. **Backup and Version Control:**
   - Created a backup and used Git to manage changes.

2. **Installing Chirpy:**
   - Updated the `Gemfile`:
     ```ruby
     gem "jekyll-theme-chirpy"
     ```
   - Ran `bundle install` to install dependencies.

3. **Configuration Adjustments:**
   - Updated `_config.yml` with Chirpy-specific options:
     ```yaml
     theme: jekyll-theme-chirpy
     ```

4. **Content Structure Update:**
   - Moved posts into categorized folders (`_posts/category_name`).
   - Updated front matter for posts to include categories and tags for better navigation.

5. **Assets Migration:**
   - Adjusted asset paths and optimized images for Chirpy\u2019s recommended resolutions.

6. **Testing:**
   - Ran `bundle exec jekyll serve` to preview and ensure everything rendered correctly.

### Pros and Cons Comparison

| Aspect               | Minima Theme                                  | Chirpy Theme                             |
|----------------------|-----------------------------------------------|------------------------------------------|
| **Design**           | Minimalistic, clean layout                     | Modern, elegant, content-rich            |
| **Customization**    | Limited customization options                  | Extensive customization through YAML     |
| **SEO**              | Basic SEO support                              | Advanced SEO integration                 |
| **Navigation**       | Simple linear navigation                       | Multi-level categories, tags, and menus  |
| **Performance**      | Lightweight, very fast load times              | Optimized but slightly heavier           |
| **Features**         | Basic blogging features                        | Enhanced features (comments, dark mode, TOC) |
| **Documentation**    | Simple and straightforward                     | Comprehensive, with community support    |

### Useful New Features in Chirpy

Switching to Chirpy has brought in several valuable features that significantly enhance user engagement and blog usability:

1. **Dark Mode:**
   - Automatic and manual dark mode toggling for a better reading experience.

2. **SEO Enhancements:**
   - Integrated support for SEO best practices (structured data, meta tags).

3. **Comments Integration:**
   - Built-in support for Disqus and Utterances, facilitating community interaction.

4. **Table of Contents (TOC):**
   - Automatically generated TOC for posts, aiding readers in navigating longer articles.

5. **Category and Tag Management:**
   - Robust organization of posts, improving discoverability and readability.

### Conclusion

The migration from **Minima** to **Chirpy** has transformed my blogging experience, offering richer features, improved user interaction, and better overall aesthetics. While Minima served well for simplicity, Chirpy caters to a broader audience and provides the tools needed for a growing and engaged blog community.

It is everything that I have for today.  
Everyone is a blacksmith of own fate.  
Mateusz.
