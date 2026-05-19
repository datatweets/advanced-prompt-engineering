# Module 1 Examples

## Example: Meeting Summary Prompt

```text
Act as an operations assistant.

Summarize the meeting notes below for a manager.

Return:
1. Key decisions
2. Open questions
3. Action items in a table with owner role, task, deadline, and risk

Rules:
- Do not invent missing details.
- Mark unclear points as "needs confirmation."
- Use concise business language.

Notes:
[paste meeting notes]
```

## Example: Study Guide Prompt

```text
Act as a study coach.

Create a study guide for the topic below.

Audience:
Students who are new to the topic.

Return:
1. Plain English explanation
2. Key terms
3. Three practice questions
4. Common mistakes
5. A short self-check quiz

Topic:
[paste topic]
```

## Example: Zero-Shot Classification Prompt

```text
Classify the customer comment as positive, neutral, or negative.

Return only one label.

Comment:
[paste comment]
```

## Example: One-Shot Classification Prompt

```text
Classify the customer comment as positive, neutral, or negative.

Example:
Comment: The setup was simple, but the reporting page is confusing.
Output:
Label: neutral
Reason: The comment includes one positive point and one negative point.

Now classify:
Comment:
[paste comment]
```

## Example: Few-Shot Classification Prompt

```text
Classify each customer comment as positive, neutral, or negative.

Example 1:
Comment: The tool saved our team several hours.
Label: positive

Example 2:
Comment: The product did not work as expected and support was slow.
Label: negative

Example 3:
Comment: The tool is useful, but the onboarding instructions need work.
Label: neutral

Now classify:
Comment:
[paste comment]
```

## Example: Step-By-Step Review Prompt

```text
Analyze the campaign idea below.

First list:
1. Goal
2. Audience
3. Assumptions
4. Missing information
5. Risks to verify

Then return a final recommendation in a table with:
Recommendation | Reason | Risk | Next step

Campaign idea:
[paste idea]
```
