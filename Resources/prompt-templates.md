# Prompt Templates

## General Business Prompt

```text
Act as [role].

Task:
[specific task]

Audience:
[audience]

Context:
[background]

Inputs:
[source material]

Constraints:
[tone, length, risks, facts to avoid inventing]

Format:
[sections, table, bullets, checklist]

Review criteria:
[what makes the answer good]
```

## Research Prompt

```text
Act as a market research assistant.

Analyze the information below.

Return:
1. Key themes
2. Evidence for each theme
3. Audience segments
4. Content opportunities
5. Assumptions that need validation

Rules:
- Use only the provided information.
- Label assumptions clearly.

Information:
[paste information]
```

## Content Draft Prompt

```text
Act as a business writing assistant.

Create [content type] for [audience].

Goal:
[goal]

Key points:
[bullets]

Tone:
Plain English, professional, useful.

Constraints:
- No unsupported claims.
- No personal names.
- No confidential information.

Format:
[desired structure]
```

## Review Prompt

```text
Review the output below.

Check for:
1. Accuracy
2. Clarity
3. Audience fit
4. Unsupported claims
5. Missing context
6. Privacy or risk concerns

Return a table with issue, severity, and recommended fix.

Output:
[paste output]
```

## Zero-Shot Prompt

Use when the task is simple and does not need examples.

```text
Task:
[specific task]

Context:
[short context]

Format:
[desired output format]

Input:
[paste input]
```

## One-Shot Prompt

Use when one example is enough to show the pattern.

```text
Use this example:

Input:
[example input]

Output:
[example output]

Now complete the task:

Input:
[new input]
```

## Few-Shot Prompt

Use when consistency matters across repeated tasks.

```text
Use these examples:

Example 1:
Input:
[example input]
Output:
[example output]

Example 2:
Input:
[example input]
Output:
[example output]

Example 3:
Input:
[example input]
Output:
[example output]

Now complete the task:

Input:
[new input]
```

## Step-By-Step Prompt

Use when the task needs planning, comparison, or review.

```text
Analyze the task step by step.

First return:
1. Goal
2. Known information
3. Missing information
4. Assumptions
5. What a human should verify

Then return the final answer in this format:
[format]

Task:
[task]
```
