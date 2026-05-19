# 02: Prompt Engineering Principles

![Principles](https://img.shields.io/badge/section-five%20principles-2563eb)

## Lesson Purpose

This lesson teaches five core prompt engineering principles and four fundamental prompting techniques. Together, they give you a repeatable system for getting useful, reliable output from any AI tool.

Prompt engineering is the practice of crafting inputs that produce outputs worth using. A good prompt reduces guessing on the model's part. A great prompt also makes the output easier to evaluate, improve, and reuse in real work.

By the end of this lesson you will be able to: write prompts that give clear direction, control output format, use examples strategically, evaluate quality systematically, and break complex work into manageable steps.

## Timing Plan

| Time | Activity | Outcome |
| ---: | --- | --- |
| 0-5 min | Compare weak and strong prompts | You see concretely why prompt quality matters |
| 5-15 min | Principles 1 and 2: Direction and Format | You control role, audience, style, and output structure |
| 15-25 min | Zero-shot, one-shot, and few-shot | You choose the right amount of examples |
| 25-35 min | Chain-of-thought and Evaluation | You check quality and ask for visible reasoning |
| 35-45 min | Divide labor | You break complex work into reliable steps |
| 45-50 min | Practice and review | You apply all five principles to one real task |

---

## The Five Principles at a Glance

| Principle | Core idea | Practical use |
| --- | --- | --- |
| Give direction | Define role, audience, style, and purpose | "Act as a customer support quality reviewer" |
| Specify format | Define the structure and rules of the response | "Return a table with issue, severity, and suggested fix" |
| Provide examples | Show what a correct answer looks like | Include an approved email reply or content sample |
| Evaluate quality | Rate or compare outputs against stated criteria | Score a draft for clarity, accuracy, tone, and risk |
| Divide labor | Split complex tasks into ordered steps | Research, outline, draft, review, then publish |

These five principles were not invented for AI. They are the same principles that govern good communication with any collaborator — human or machine. What makes them essential with AI is that the model will not push back, ask for clarification, or refuse a vague task. It will always produce something. Your job is to make sure that something is useful.

---

## Principle 1: Give Direction

Direction tells the model who it is, who it is speaking to, and what it is trying to accomplish. Without direction, the model produces a generic answer aimed at no one in particular.

Direction is composed of several layers:

| Layer | What to specify | Example |
| --- | --- | --- |
| Role | Who the model should act as | "Act as a market research analyst" |
| Audience | Who will read the output | "For managers with no prior AI experience" |
| Style | Tone and register | "Plain English, professional, no jargon" |
| Goal | What the reader should think, feel, or do | "Help the reader decide whether to adopt this tool" |
| Boundaries | What the model must not claim or assume | "Do not make legal or financial claims" |

### Weak vs. Strong: A Direct Comparison

**Weak prompt:**
```text
Write about AI.
```
This produces a general, surface-level essay. The model has no idea whether you want an elevator pitch, a risk analysis, a beginner's guide, or a technical overview.

**Strong prompt:**
```text
Act as a workplace training assistant.

Write a plain English explanation of how generative AI can help managers 
prepare weekly reports faster and more accurately.

Audience:
Managers who are busy, skeptical of hype, and responsible for accuracy.

Style:
Direct, practical, no buzzwords.

Constraints:
- Do not claim AI is always accurate.
- Do not use the word "revolutionary" or similar hype language.
- Keep the total response under 300 words.
```

The second prompt gives the model five pieces of direction: role, topic, audience, style, and constraints. The output will be dramatically more usable.

> **Tip:** The most powerful direction element is the role. When you tell the model to "act as" someone specific — a curriculum designer, a legal editor, a plain-language translator — it shifts the tone, structure, and vocabulary of the response in ways that are hard to achieve through constraints alone.

---

## Principle 2: Specify Format

Output format determines whether you can actually use the result. An AI answer in loose paragraph form may take an hour to extract, reorganize, and clean up. The same content in a table, checklist, or structured template might be usable immediately.

Format is not just about aesthetics. It is about workflow. The output of one AI task often becomes the input to the next task, another tool, or a human review step. If the format is wrong, the whole chain breaks.

### Useful Output Formats

| Format | Best for |
| --- | --- |
| Numbered list | Steps, recommendations, priorities |
| Table | Comparisons, status tracking, analysis output |
| JSON | Technical workflows, structured data, API inputs |
| Checklist | Review steps, quality criteria, compliance items |
| Email draft | Customer replies, internal communication |
| Outline | Article structure, presentation plan, training module |
| Storyboard table | Video scripts, lesson plans, slide sequences |
| Prompt template | Reusable instructions with fill-in-the-blank slots |

### Format Specification Example

```text
Return a table with these five columns:

Audience segment | Core pain point | Supporting evidence | 
Content idea | Confidence level (high / medium / low)

Do not leave any cell blank. If evidence is missing, write "hypothesis — needs validation."
```

This level of format specification means the output arrives ready to discuss, prioritize, or share — not ready to clean up.

> **Key insight:** The more specific your format, the less editing you need to do afterward. A well-specified format is worth as much as a well-written instruction.

---

## Principle 3: Provide Examples

Examples teach the model what "correct" looks like for your specific situation. Generic instructions tell the model what to do; examples show it how to do it.

There are three levels of example usage, each suited to different situations:

### Zero-Shot Prompting

Zero-shot means asking directly, without examples. You describe the task and trust that the model's training has given it enough context to respond correctly.

**When it works well:**
- The task is common (summarizing a document, classifying sentiment).
- The output format is simple and standard.
- You are exploring ideas quickly and the cost of an imperfect first draft is low.

**Example:**
```text
Classify the customer comment below as positive, neutral, or negative.

Return only one label.

Comment:
The product is easy to use, but setup took longer than expected.
```

**The risk:** For specialized, nuanced, or organization-specific tasks, the model may guess the wrong format, tone, or criteria.

---

### One-Shot Prompting

One-shot means giving one example before the task. It is the fastest way to show the model what a correct output looks like without overloading the prompt.

**When it works well:**
- The output must follow a specific pattern.
- The task has a preferred answer style that is hard to describe in words.
- You have a strong, representative example to use.

**Example:**
```text
Classify each customer comment using the format below.

Example:
Comment: The support team answered quickly, but the documentation was confusing.
Label: neutral
Reason: Positive support experience, negative documentation experience — mixed overall.

Now classify this comment:
Comment: The product helped our team save two hours a week, and setup was straightforward.
```

**The risk:** One example can bias the output. If your example is unusual, the model may overgeneralize from it.

---

### Few-Shot Prompting

Few-shot means providing two or more examples before the task. This is the most reliable technique for tasks that need consistency: classification, style matching, structured output, or repeated workflows.

**When it works well:**
- You need consistent output across many items (classifying 50 comments, formatting 20 summaries).
- The desired tone or structure is specific to your brand or team.
- You have reviewed and approved the examples.

**Example:**
```text
Classify each product review as positive, neutral, or negative.

Example 1:
Review: Completely useless. Support never replied.
Sentiment: negative

Example 2:
Review: Works well for our team, though onboarding took a few days.
Sentiment: neutral

Example 3:
Review: Fast, easy to use, and support resolved our issue within an hour.
Sentiment: positive

Now classify this review:
Review: The new dashboard saves us time on reporting, 
but the export function still crashes occasionally.
Sentiment:
```

**The risk:** Too many examples consume significant context. Keep examples short, representative, and directly relevant.

---

### Choosing the Right Level

| Situation | Recommended level |
| --- | --- |
| Quick draft, standard format | Zero-shot |
| Need to show a specific format or tone | One-shot |
| Need consistency across many items | Few-shot |
| Unusual task or specialized output | Few-shot with evaluation |

---

## Principle 4: Evaluate Quality

Generating output is only half the work. The other half is knowing whether the output is any good. This requires defining quality criteria before you read the answer.

Evaluation in prompt engineering has two forms:

**Form 1: Self-evaluation** — Ask the model to review its own output against specific criteria.

**Form 2: External criteria** — You define what a good answer looks like and check the output yourself.

Both forms are useful. The first is faster. The second is more reliable for important work.

### Self-Evaluation Prompt

```text
Review your previous answer and score it from 1 to 5 on each criterion:

1. Accuracy: Are all claims supportable?
2. Clarity: Would a non-expert understand this without difficulty?
3. Audience fit: Does it speak directly to the target reader?
4. Practical usefulness: Does it give the reader something to act on?
5. Risk: Does it make any unsupported claims or recommendations?

Return a table with: criterion, score, reason, and suggested improvement.
```

### Evaluation Table: What Good Looks Like

| Criterion | Weak output | Strong output |
| --- | --- | --- |
| Accuracy | Makes claims without evidence | Uses only provided facts; marks assumptions |
| Clarity | Contains jargon without explanation | Plain English throughout |
| Audience fit | Generic — could be for anyone | Addresses the specific reader's situation |
| Usefulness | Explains without guiding | Gives a workflow, checklist, or decision tool |
| Risk control | Presents all output as ready to use | Flags where human review is needed |

> **Important:** Do not assume the model's self-evaluation is honest. It will tend to score itself highly. Use self-evaluation as a starting point, not a final verdict. You are the judge.

---

## Principle 5: Divide Labor

Complex work produces better results when it is broken into steps. Each step becomes a focused prompt with a clear input and output. The output of one step becomes the input of the next.

This principle mirrors good project management: you would not ask a new team member to "write the whole report" without agreeing on the audience, structure, and tone first.

### The Staircase Pattern

Instead of:
```text
Create a complete marketing strategy for our product.
```

Use a sequence:
```text
Step 1:
Ask me five questions about the target audience that you need answered 
before building a strategy.

Step 2:
Based on my answers, identify the top three audience segments and their 
primary concerns.

Step 3:
Propose three content themes that address those concerns.
Format: table with theme, audience, and rationale.

Step 4:
Draft one content piece for the highest-priority theme.

Step 5:
Review the draft for accuracy, tone, and missing information.
Return a risk and quality table.
```

Each step is reviewable. You can correct direction between steps. Nothing gets wasted if the first step goes wrong.

### When to Divide Labor

Divide complex tasks when:
- The task has multiple distinct phases (research, planning, drafting, review).
- A mistake in step one would ruin all subsequent steps.
- Different people are responsible for different steps.
- The output requires human review or approval at a specific point.
- The task involves judgment calls that benefit from a pause.

---

## Chain-of-Thought Prompting

Chain-of-thought prompting is a specific form of labor division that asks the model to show its reasoning before giving an answer. Originally developed for complex reasoning tasks, it is useful in business contexts when the process needs to be auditable.

### Basic Form

```text
Before giving your final recommendation, work through the following steps:

1. Summarize the situation.
2. List the key assumptions you are making.
3. Identify what information is missing.
4. Note the main risks.
5. Then give your recommendation.
```

### When to Use It

Use chain-of-thought prompting when:
- The answer depends on assumptions that should be visible.
- The output will be reviewed by someone other than you.
- The problem has multiple valid interpretations.
- The task involves calculation, diagnosis, or prioritization.

Use it sparingly when:
- The task is simple.
- The intermediate reasoning would expose private input data.
- You need a short, clean output with no extra commentary.

---

## The Anatomy of a Well-Built Prompt

The five principles tell you what to think about. This anatomy gives you the exact parts to write. Use it as a checklist for any prompt that will be used in real work.

| Part | What it is | Example |
| --- | --- | --- |
| Task | One specific action with a verb | "Write a 200-word summary for a department manager" |
| Scope | What is included and what is excluded | "Cover only January to March. Do not include budget projections." |
| Context | Background material the model needs | Paste source documents, meeting notes, or relevant data |
| Reference | A sample that shows the desired tone or format | "Match the format and tone of this approved summary: [paste example]" |
| Success brief | What a complete, correct output looks like | "Output: three bullets, under 20 words each, direct tone, no jargon" |
| Rules | Positive instructions about how to write | "Write so a 16-year-old could read it aloud" |
| Source constraint | What to use — and what not to invent | "Use only the provided source material. Do not add external claims." |
| Plan | Ask the model to state its assumptions first | "Before writing, list your three key assumptions and one risk to flag" |

**Two principles that apply to every part:**

First, convert every "don't" into a "do." Instead of "don't use jargon," write "use plain English, the kind you would use in a spoken conversation." Positive instructions are clearer and produce more consistent results.

Second, write the success brief before the rules. Knowing exactly what a good output looks like makes it far easier to write the constraints and instructions that get you there.

---

## Nine Techniques That Sharpen Any Prompt

The five principles are your strategy. These nine techniques are tactical adjustments that produce measurably better results on everyday tasks. You do not need to use all nine at once — start with the first three and add others as you practice.

**1. Name the output, not the task**

Vague verbs get vague drafts. Replace "review," "help with," or "look at" with the exact deliverable.

| Weak | Strong |
| --- | --- |
| Review my email | Write a revised version of this email that is 30% shorter and uses plain English throughout |
| Help with my plan | Return a five-item prioritized action plan in a two-column table: action and owner role |
| Look at these notes | Extract three key decisions and flag any items that need human confirmation |

**2. Define the length up front**

Set the exact count. "Three bullets, under 20 words each" produces very different output than "a few key points." The model has no natural sense of length unless you give it a target.

**3. Turn every "don't" into a "do"**

Find every "avoid," "don't," or "never" in your prompt and rewrite it as a positive instruction.

| Negative | Positive |
| --- | --- |
| Don't use corporate speak | Write in plain, conversational English — the kind you would use explaining this to a friend |
| Don't make it too long | Keep the total response under 150 words |
| Don't be vague | Every recommendation must name a specific, actionable next step |

**4. Lead with an action verb**

Start the task line with a verb: Write. Find. Draft. Classify. Compare. Summarize. The first word signals exactly what type of response to produce. Politeness costs context. Action moves work forward.

**5. Ask for reasoning before the answer**

On complex tasks, add: "Before answering, think through the problem step by step and list your assumptions." The model produces more considered, auditable output when reasoning is visible before the conclusion.

**6. Set a quality standard, not just a format**

End your prompt with one sentence that describes what a good output looks like: "A strong response gives a manager something to act on in under five minutes." This acts as a bar the model tries to reach — not just a shape to fill.

**7. Bring your own voice**

Paste two or three sentences written exactly the way you actually sound. Tell the model to match that style. Generic prompts produce generic results. Your actual writing — even three sentences — shifts the output immediately toward something that sounds like you rather than like everyone else.

**8. State the goal before the task**

Open with what success looks like: "Goal: help a first-time manager understand AI risk without technical terms." Then give the task. A prompt without a stated goal is a guess. A prompt with a goal is a brief.

**9. Name what the model must not assume**

Add a brief line for any assumption the model might make incorrectly: "Do not assume the reader has prior AI experience." "Do not invent statistics." "Do not recommend specific tools by name." Eliminating wrong assumptions is faster than correcting wrong output after the fact.

---

## Weak and Strong Prompts: Five More Pairs

Reading weak and strong prompts side by side is one of the fastest ways to internalize what specificity actually means. Each pair below shows the same request rewritten with audience, purpose, scope, and format added.

| Weak prompt | What is missing | Stronger version |
| --- | --- | --- |
| Can you give me book recommendations? | Genre, purpose, audience, time frame | Can you recommend three science fiction novels from the last five years that explore AI and society, for a non-technical business reader who commutes by train? |
| What's the best computer? | Use case, budget, key criteria | What is the best laptop for video editing under $2,000 this year, considering rendering speed, display quality, and portability? |
| Tell me about Shakespeare. | Scope, angle, purpose | Analyze the themes of ambition and power in Macbeth for a student writing a 1,000-word comparative essay. |
| How to make a cake? | Type, detail level, audience | What are the steps to baking a classic French Genoise sponge cake? Include common mistakes and how to avoid them, for a beginner baker. |
| What's the weather? | Location, date, specific variable | What is the forecast for a coastal business district on a summer Saturday, focusing on humidity and the probability of rain? |

The pattern is identical in every pair: weak prompts omit audience, purpose, scope, and format. Adding all four — even briefly — is what turns a vague question into a useful brief.

---

## Technique 10: Using AI to Improve Your Own Prompts

The nine techniques above tell you how to write better prompts. There is also a faster path when a prompt is not working: give it to AI and ask it to improve it.

This works because AI has processed enough well-structured prompts to recognize what good prompting looks like. Give it a weak prompt and a description of what you want the output to look like, and it will suggest direction, format, examples, and constraints you forgot to include.

**The meta-prompt:**

```text
You are an expert in prompt engineering.

I have a prompt that is not producing the results I need.

Current prompt:
[paste your current prompt]

What I actually want the output to look like:
[describe or show one example of a good response]

Improve the prompt by:
1. Adding a clear role and audience.
2. Specifying the output format exactly.
3. Adding one example of a correct response.
4. Replacing vague instructions with specific ones.
5. Adding a quality criterion — one sentence that describes what a good response achieves.

Return only the improved prompt, nothing else.
```

> **Tip:** Run the optimized version alongside your original and compare the outputs. The AI-improved version will often surface a requirement you forgot to include — which tells you something important about what your original prompt was missing.

Use this technique when:
- A prompt has failed three or more times and the output still feels wrong.
- You can describe what a good output looks like but cannot figure out how to ask for it.
- You want to turn a one-off prompt into a clean, reusable template.

Do not use it when:
- The task is already fully specified — additional complexity is unnecessary.
- You have not yet run the prompt at all. Try it first, then optimize.

---

## Putting All Five Principles Together

Here is a single prompt that applies all five principles:

```text
Role:
Act as a content strategist for a corporate training team.

Task:
Create a two-week content calendar for an AI productivity course 
targeting business owners, managers, employees, and students.

Audience:
Marketing and curriculum team. They need a plan they can implement 
without AI expertise.

Context:
The course launches in three weeks. We have one blog post, one email, 
and one professional network account. Resources are limited.

Format:
Return a table with:
Week | Day | Channel | Audience | Journey stage | Message angle | 
Asset type | Owner role | Review step

Constraints:
- No personal names.
- No unsupported claims about outcomes or statistics.
- Keep the plan realistic for a two-person team.
- Flag any item that requires legal or compliance review.

Examples:
Week 1 | Monday | Professional network | Business owners | Awareness | 
How AI reduces time spent on weekly reports | 
Short post | Content lead | Marketing manager review

Quality criteria:
A good plan has consistent message angles per audience, a realistic cadence, 
and a review step for every customer-facing item.

Step-by-step check:
Before returning the table, briefly state:
1. Your assumption about the available content
2. Any missing information that would improve the plan
3. One risk to flag
```

This prompt is longer than a beginner would write at first. You will reach this level naturally through practice over the following lessons.

---

## Practice

**Rewrite this weak prompt using all five principles:**

```text
Make content for my business.
```

Your improved prompt must include:
- Role for the model.
- Specific audience with context.
- Clear output format with column names.
- One example of the desired output style.
- At least one quality criterion.
- A division into at least two steps.

Then create four variations:
1. Zero-shot version.
2. One-shot version with one example.
3. Few-shot version with three examples.
4. Step-by-step version that asks for assumptions and checks before the final answer.

---

## Review Checklist

- [ ] Does your prompt tell the model who it is acting as?
- [ ] Does it specify the exact format of the output?
- [ ] Does it use zero-shot, one-shot, or few-shot appropriately for the task?
- [ ] Does it include quality criteria or ask for self-evaluation?
- [ ] For complex tasks, is it split into steps?
- [ ] Does it include at least one constraint that prevents risky output?
