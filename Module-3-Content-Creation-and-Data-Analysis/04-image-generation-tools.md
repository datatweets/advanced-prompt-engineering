# 04: Image Generation Tools — Bonus Lesson

![Bonus](https://img.shields.io/badge/section-image%20generation-f97316)

## Lesson Purpose

This bonus lesson teaches you to write prompts for the three most widely used AI image generation tools: DALL-E, Midjourney, and Stable Diffusion. Each tool has a different syntax, a different strength, and a different level of technical control. Understanding the differences lets you choose the right tool for each content job and write prompts that produce usable results the first time.

The core principle is the same as in text prompting: specificity produces better output. A vague prompt like "office meeting" produces a generic stock photo. A specific prompt with subject, style, lighting, and technical modifiers produces something your content team can actually use.

## Timing Plan

| Time | Activity | Outcome |
| ---: | --- | --- |
| 0-10 min | Compare the three tools | You choose the right tool for each content type |
| 10-20 min | Anatomy of an image prompt | You identify the four parts every image prompt needs |
| 20-30 min | DALL-E prompts | You write natural-language image prompts in plain English |
| 30-40 min | Midjourney prompts | You apply style weights, aspect ratios, and negative parameters |
| 40-50 min | Stable Diffusion prompts | You use positive + negative prompts and seed control |
| 50-60 min | Templates and practice | You build reusable image prompt templates |

---

## The Three Tools at a Glance

| Tool | Prompt style | Strongest use case | Technical control |
| --- | --- | --- | --- |
| DALL-E | Natural language — describe it in plain English | Integrated workflows, quick business visuals, accessible for beginners | Low — no special syntax needed |
| Midjourney | Style-heavy — subject + artist + parameters | High-quality artistic images, visual marketing, campaign assets | Medium — uses parameters like `--ar`, `--no`, `--v` |
| Stable Diffusion | Technical — positive prompt + negative prompt + seed | Full control over output, reproducibility, product images, batch generation | High — requires understanding of models and parameters |

> **Key insight:** DALL-E rewards good writing. Midjourney rewards style vocabulary. Stable Diffusion rewards technical setup. Match the tool to what you are good at — and what the content job requires.

---

## Anatomy of an Image Prompt

Every image prompt has four building blocks, regardless of which tool you use:

| Part | What it controls | Example |
| --- | --- | --- |
| Subject | What is in the image | "A manager reviewing a document at a clean desk" |
| Style | How the image looks | "In the style of corporate photography", "oil painting", "surrealism" |
| Quality modifiers | Level of detail and realism | "Photorealistic", "extremely detailed", "studio lighting", "35mm DSLR" |
| Technical specs | Format and composition | Aspect ratio, resolution, camera angle |

A useful image prompt usually includes all four. A quick draft only needs subject and style. A production-ready prompt for a campaign asset needs all four.

> **Tip:** Before writing any image prompt, define the content job first: Who will see this image? What should they feel? What format does it need to be? These answers determine which parts of the anatomy matter most.

---

## DALL-E: Natural Language Image Prompts

DALL-E is the most accessible of the three tools. You describe the image in plain English — the same way you would describe it to a designer. It does not require a special syntax or parameters.

**Basic structure:**
```text
[Shot type or composition] of [subject], [style], [lighting], [background or setting].
```

**Simple example:**
```text
A golden gate bridge at sunset in the style of surrealism,
dreamlike colours, warm light.
```

**Business content example:**
```text
An illustration of a business meeting with four people watching a laptop screen,
in the style of Corporate Memphis, white background, professional clean lines,
warm pastel colours.
```

**DALL-E prompt rules:**

| Rule | Why it matters |
| --- | --- |
| Describe what you want — not what you do not want | DALL-E handles positive instructions better than negatives |
| Specify style explicitly | Without a style instruction, you get a neutral photo-realistic result |
| Include setting and lighting | "Clean white background, soft studio lighting" changes the entire tone |
| Keep the description sequential | Subject → style → setting → mood works better than mixed order |

> **Note:** DALL-E integrates directly with ChatGPT, which means you can iterate in conversation: generate an image, describe what to change, and regenerate without rewriting the full prompt.

---

## Midjourney: Style-Heavy Prompts with Parameters

Midjourney produces some of the most visually striking AI images available. It favours rich style descriptions and uses a parameter syntax to control aspect ratio, version, and what to exclude.

**Basic structure:**
```text
[Subject and action], [style descriptor], [mood or lighting] --ar [ratio] --v [version]
```

**Simple examples from practice:**
```text
golden gate bridge in the style of surrealism
```

```text
dark knight rises wallpapers, in the style of dusan djukaric,
dark sky-blue, dynamic and intense --ar 30:17 --v 5
```

```text
a spiderman standing in a city with explosions above him,
in the style of emotive body language, movie poster --ar 30:17 --v 5
```

**Key Midjourney parameters:**

| Parameter | What it does | Example |
| --- | --- | --- |
| `--ar` | Sets the aspect ratio | `--ar 2:1` for wide banner, `--ar 9:16` for portrait |
| `--no` | Excludes elements from the image | `--no cartoon` to force realistic style |
| `--v` | Sets the model version | `--v 6` for the latest version |

**Multi-prompt weighting:**

You can give different elements different importance using `::` notation. A positive number increases weight; a negative number suppresses that element.

```text
golden gate bridge:: by van gogh::0.9 by picasso::0.1 clouds::-1
```

This tells Midjourney: emphasize Van Gogh's style, add a small Picasso influence, and remove clouds entirely.

**Character and composition consistency:**
```text
two images side by side, rockstar American rough-and-ready middle-age actor,
photo booth portrait --ar 2:1

side profile image, rockstar American rough-and-ready middle-age actor,
photo booth portrait --ar 2:1
```

Combining consistent descriptions with the same `--ar` and composition instructions produces a set of images that work together as a series.

**Batch variation with templates:**

You can plan multiple image variations from one template by swapping one element at a time:

```text
{stock photo, oil painting, illustration} of a business meeting
of {four, eight} people watching a laptop on a glass-top table
```

Running this prompt generates six variations covering both style and group size — useful when you need multiple assets for the same content.

> **Tip:** Build a small personal dictionary of art styles and photographers that match your brand. Midjourney responds well to references like "in the style of corporate photography, Panasonic DC-GH5" or "Corporate Memphis, warm pastels". Keep a running list of style terms that consistently produce on-brand results.

---

## Stable Diffusion: Positive and Negative Prompts with Seed Control

Stable Diffusion gives you the most technical control of the three tools. The key difference is the **negative prompt** — a separate list of what you do not want the image to include. This makes Stable Diffusion the right choice when you need repeatable, production-quality results.

**Structure:**
```text
Prompt (positive):
[Subject, style, quality modifiers, technical specs]

Negative prompt:
[What to exclude: quality issues, unwanted elements, unwanted styles]

Seed:
[Number for reproducibility]
```

**Example from practice:**
```text
Prompt:
anime cat girl with pink hair and cat ears outfit posing for a picture,
photorealistic, character portrait, floral print, sunlight, wavy hair,
looking at viewer, official art, sots art

Negative:
disfigured, ugly, bad, immature, photo, amateur, overexposed, underexposed

Seed:
3588970703
```

**Another example — product image:**
```text
Prompt:
neon pink and blue sneakers, intricate design, beautiful, platemail armor details,
sleek iridescent finish, product photography, extremely detailed,
studio lighting, 35mm, DSLR

Negative:
soft, misshapen, corners, straps, laces
```

**Key Stable Diffusion concepts:**

| Concept | What it controls | When to use |
| --- | --- | --- |
| Positive prompt | Everything you want in the image | Always — this is the core description |
| Negative prompt | Artefacts, unwanted styles, quality issues | Always — prevents common output problems |
| Seed | A fixed number that makes the output reproducible | When you need to produce the same image again or make small variations on a base result |
| Model selection | The underlying model changes style and capabilities | When you need a specific look — photorealistic, anime, illustration |

**Common negative prompt terms for business content:**
```text
disfigured, deformed, ugly, blurry, low quality, amateur, overexposed,
underexposed, watermark, text, logo, extra limbs
```

This base negative prompt prevents the most common quality failures. Add to it based on what you see in your outputs.

> **Warning:** Stable Diffusion requires more setup than DALL-E or Midjourney. It works through local installation or third-party platforms. If your team is new to image generation, start with DALL-E for accessibility or Midjourney for quality, and move to Stable Diffusion when you need reproducibility and full control.

---

## Detailed Style Descriptions

When you need a specific visual style that is hard to name in one word, describe it in detail. This technique works in all three tools.

**Example — Surrealist painting style:**
```text
Give me a painting of Times Square in the following style:

Surrealist art movement — dreamlike, irrational, fantastical imagery.
Characteristics:
- Melting, fluid forms: people and objects appear to melt and drape over surfaces
- Expansive barren landscape in the background
- Hyper-realistic detail in textures despite surreal content
- Pastel palette with blurred edges in background areas
- Soft, diffused light with almost photographic foreground detail
```

This level of description gives AI enough visual vocabulary to produce something substantially different from a generic "surrealist painting."

---

## Business Use Cases

| Content job | Recommended tool | Prompt approach |
| --- | --- | --- |
| Blog post header image | DALL-E | Natural language, Corporate Memphis style, white background |
| Campaign hero image | Midjourney | Style-heavy, `--ar 16:9`, brand colour palette |
| Social media post variations | Midjourney | Template with `{style1, style2}` for batch output |
| Product photography mock-up | Stable Diffusion | Detailed positive prompt, strong negative prompt, seed for consistency |
| Internal presentation visual | DALL-E | Clean, professional, illustration style |
| Storyboard scene reference | Any tool | Subject + composition + lighting — used as visual brief, not final asset |

> **Key insight:** AI-generated images should be treated as starting points for most professional uses — not finished assets. Use them to brief designers, test visual directions, or produce rough drafts that a human refines. Save them as final assets only for internal use or low-risk content.

---

## Responsible Use

Image generation tools raise specific responsibilities that text generation does not:

| Risk | What it means | What to do |
| --- | --- | --- |
| Copyright and style | Some art style prompts reference living or recently deceased artists | Check your organization's policy on referencing named artists. Use broad style terms ("surrealism", "impressionism") when in doubt. |
| Likeness | Named real people in prompts can produce misleading images | Do not generate images of real, identifiable people for marketing or public content. |
| Misleading content | Photo-realistic AI images can be mistaken for real photographs | Label AI-generated images clearly when required by your organization or platform. |
| Brand consistency | AI images may not match your brand guidelines | Always review against your brand guide before publishing. |
| Model terms of service | Each tool has different commercial use rules | Check the specific tool's commercial license before using images in paid campaigns. |

> **Important:** The same review standard that applies to AI text applies to AI images. Every image used in public-facing content should have a human review step before publishing.

---

## Practice

**Exercise 1: Style comparison**

Take one subject — a professional workspace, a team meeting, or a product — and write prompts for the same image in three different styles:
1. Corporate Memphis illustration
2. Photorealistic studio photography
3. A named fine-art style (impressionism, surrealism, or similar)

Compare the outputs across tools if you have access to more than one.

**Exercise 2: Positive and negative prompt pairs**

Write a prompt for a business image. Then write its negative prompt — the 5 to 10 terms that would most likely ruin the image. Run both and compare.

**Exercise 3: Storyboard to image brief**

Take one scene from the storyboard you created in Lesson 3. Write a full image prompt for that scene using the four-part anatomy: subject, style, quality modifiers, and technical specs.

---

## Review Checklist

- [ ] Does your prompt define subject, style, quality modifiers, and technical specs?
- [ ] Have you matched the tool to the content job — DALL-E for quick, Midjourney for style, SD for control?
- [ ] If using Stable Diffusion, does the prompt include a negative list?
- [ ] If using Midjourney, have you added `--ar` for the correct format?
- [ ] Have you reviewed the output against your brand guide before using it?
- [ ] Is the image labeled as AI-generated where required?
- [ ] Have you confirmed the tool's commercial license if this is for a paid campaign?
