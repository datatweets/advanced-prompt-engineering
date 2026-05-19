# 01: Responsible AI Use

![Ethics](https://img.shields.io/badge/section-responsible%20AI-7c3aed)

## Lesson Purpose

This lesson teaches you how to use AI responsibly in business, corporate, and educational settings. It covers the most common failure modes — hallucinations, privacy leaks, unsupported claims, bias, and overreliance — and gives you practical prompt structures and review workflows to manage each one.

Responsible use is not a separate track from effective use. Every skill in this course — the five principles, research workflows, content creation — only holds its value if the output is accurate, appropriate, and safe to publish or send.

## Timing Plan

| Time | Activity | Outcome |
| ---: | --- | --- |
| 0-5 min | Establish the core principle | You understand that responsibility follows the person, not the tool |
| 5-15 min | Identify risk categories | You recognize the six main risks and their controls |
| 15-25 min | Build a safer prompt | You write prompts with built-in safeguards |
| 25-35 min | Run a risk review | You use a structured review table on real output |
| 35-45 min | Build a human review checklist | You define the review steps your work requires |
| 45-50 min | Discuss edge cases | You apply responsible use to ambiguous scenarios |

---

## The Core Principle

AI can draft, organize, classify, summarize, and suggest. People remain responsible for deciding whether the output is accurate, appropriate, lawful, and ready to use.

This is not a legal disclaimer. It is the operating reality of every AI tool available today. These systems:

- Generate fluent, confident text that may be factually wrong.
- Cannot verify their own outputs.
- Do not know your company's internal policies.
- Cannot distinguish public information from private data you paste in.
- Reflect biases present in their training data.

None of these limitations make AI useless. They make a structured review process essential.

> **Important:** The more polished the output, the easier it is to trust it without checking. This is backwards. Polished output that is wrong is more dangerous than rough output that is wrong — because it is more likely to be published, sent, or acted on without review.

---

## Risk Categories

| Risk | What can happen | Real example | Control |
| --- | --- | --- | --- |
| Hallucination | AI invents facts, quotes, statistics, or sources | A market research summary with a fake industry report cited | Ask for evidence; verify all claims before using |
| Privacy leak | Sensitive data shared with an unapproved tool | A support agent pastes customer account details into a consumer AI app | Strip private data; use only approved tools |
| Unsupported claim | Output includes guarantees or statistics without proof | "AI saves teams 30% of their time" with no source | Use placeholders; require sources for all statistics |
| Bias | Output makes unfair assumptions about groups or individuals | Persona content that assumes technical roles are held by men | Review language, examples, and criteria |
| Overreliance | Team accepts polished output without review | A legal team sends an AI-drafted contract clause without checking accuracy | Require human review; never skip it for high-stakes content |
| Context error | Output misses internal policy or business reality | A draft reply offers a refund period that does not exist | Provide context; mark unknowns explicitly |

---

## Hallucination: The Most Misunderstood Risk

Hallucination is not a random malfunction. It is a predictable feature of how language models work. When a model is asked a question it does not have confident training data for, it does not say "I don't know" — it generates what looks like a plausible answer.

Signs that output may contain hallucinations:

- Specific statistics with no source mentioned.
- Quoted experts you cannot find in a web search.
- Historical claims that sound right but feel unfamiliar.
- Numbers that are oddly round or suspiciously convenient.
- External citations that cannot be verified.

The mitigation is not to avoid AI — it is to use grounding (providing your own source material) and to run a verification step on any claim you intend to publish or present.

> **Warning:** Asking AI "Are you sure this is correct?" is not a verification step. The model will say yes — confidently. Real verification means checking the claim against an external, primary source.

---

## Privacy: What to Never Paste

Before using any AI tool for work, establish a clear rule about what data stays out.

**Never paste into a consumer AI tool (unless your IT and legal team has specifically approved it):**

| Data type | Examples |
| --- | --- |
| Customer personal information | Names, emails, addresses, account numbers |
| Financial data | Revenue figures, pricing strategy, negotiation terms |
| Employee information | Performance records, compensation, HR notes |
| Legal or compliance documents | Contracts, ongoing disputes, regulatory filings |
| Proprietary processes | Internal workflows, trade secrets, IP-sensitive procedures |
| Health or medical information | Any personal health detail |

When in doubt, substitute with placeholder text:

- Replace "John Smith at Acme Corp owed us $4,200 in October" with "Customer A owed us [amount] in [month]."
- The AI can still help with the task. The sensitive information stays protected.

---

## Scenario: Customer Support with AI

A customer support team wants to use AI to draft replies faster. Some customer messages include order details, account information, and complaints about specific transactions.

The risks are real:
- Pasting customer details into an unapproved tool may violate data protection agreements.
- AI may invent a policy, refund timeline, or offer that the company does not actually have.
- A polished, confident draft may go out without review.

The solution is a prompt designed around these constraints from the start.

---

## Safer Drafting Prompt

```text
Act as a customer support drafting assistant.

Task:
Draft a reply to the customer message below.

Important rules:
- Do not include any private customer data in the output.
- Do not invent or assume any policy, refund timeline, delivery estimate, 
  or account detail.
- If information is missing or needs confirmation, write 
  "[needs confirmation from account team]."
- Use a calm, professional, and non-defensive tone.
- End with a clear next step the customer can take.

Output format:
1. Draft reply
2. List of items that need human confirmation before this reply is sent
3. Risk notes for the reviewer (anything they should double-check)

Customer message (redact all private data before pasting):
[paste redacted message here]
```

The key features of this prompt:

- "Do not invent policy" prevents the most common failure in support drafting.
- "[needs confirmation]" placeholders make the review step easy.
- The output format separates the draft from the review items — so the reviewer knows exactly where to focus.

---

## Risk Review Prompt

After any significant AI-generated output, run this review before publishing, sending, or presenting:

```text
Act as a responsible AI output reviewer.

Review the draft below.

Check for:
1. Any claim that cannot be verified from the provided source material.
2. Any private data that should not appear in the output.
3. Any unsupported statistics, quotes, or external references.
4. Any language that makes assumptions about groups of people.
5. Any tone that could feel dismissive, condescending, or defensive.
6. Any item that requires confirmation before this leaves the team.
7. Any place where human judgment is required and was not noted.

Return a table with:
Issue | Risk level (high/medium/low) | Why it matters | Recommended fix

Draft:
[paste draft here]
```

---

## Human Review Checklist

Use this checklist before any AI output leaves your desk:

- [ ] Are all factual claims verified against a primary source?
- [ ] Are sources cited for statistics, outcome claims, and external references?
- [ ] Is no private data present in the output?
- [ ] Does the output follow current company policy?
- [ ] Are all assumptions marked and not treated as facts?
- [ ] Is the tone appropriate for the audience?
- [ ] Could any part of this output harm a customer, employee, or student if wrong?
- [ ] Has a human with the appropriate authority reviewed and approved this?

For high-stakes content — legal, financial, medical, HR, compliance — add an additional specialist review step. The AI draft is a starting point, not a first draft ready for review.

---

## Responsible Use in Practice: The Review Spectrum

Not every piece of AI-assisted work requires the same level of review. Use this spectrum as a guide:

| Content type | Review required | Who reviews |
| --- | --- | --- |
| Internal brainstorming notes | Light — quick read | Creator |
| Meeting summary for the team | Standard — accuracy check | Creator |
| Customer-facing reply | Standard — fact and policy check | Creator + team lead |
| Published blog or article | Full — claims, tone, sources | Creator + editor |
| Public claim with statistics | Thorough — source verification | Creator + subject expert |
| Legal, financial, or compliance content | Required expert review | Creator + qualified professional |

---

## Practice

Take one AI-generated output you have created in this course — a blog section, a competitor analysis, a persona, a social post, or any draft.

Run the risk review prompt and produce:

1. A risk table with at least four issues identified (even if minor).
2. A revised version of the draft that addresses each issue.
3. A custom human review checklist tailored to this content type.
4. At least one item marked as "requires confirmation" that you would not publish without checking.

---

## Review Checklist

- [ ] Can you explain in one sentence why each risk category matters in a real workplace?
- [ ] Does your safer prompt include at least three explicit safeguards?
- [ ] Does your risk review table separate facts from inferences?
- [ ] Does your human review checklist specify who reviews, not just that review happens?
- [ ] Have you identified the one output in this course most in need of a responsible use review?
