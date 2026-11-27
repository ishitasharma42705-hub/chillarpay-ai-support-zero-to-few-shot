# chillarpay-ai-support-zero-to-few-shot
Fictional FinTech case study: testing when zero-shot prompting is enough and how few-shot prompting improves AI customer-support triage for a UPI app. Includes synthetic data, prompts, AI outputs and a scorecard.
# ChillarPay AI Support: From Zero-shot to Few-shot Prompting

**A FinTech case study on when a simple prompt is enough and when AI needs examples.**

Author: Ishita · BBA (FinTech), Chitkara Business School · Tool: chatgpt · November 2026

## The case

**ChillarPay** (fictional) is a UPI payments app in Jaipur with 8 lakh users. It receives about 2,000 support messages a day in English and Hinglish, and urgent fraud cases get lost among simple questions. As a Business Analyst, I tested whether AI can sort messages, set priority and draft replies, and what kind of prompt it needs.

## The data

12 synthetic customer messages created with AI (8 English, 4 Hinglish, 3 deliberately tricky). I wrote the correct answers myself before testing.

## Approach

| Step | Prompt type | Task |
| --- | --- | --- |
| 1 | Zero-shot | One-line summary of each message |
| 2 | Zero-shot | Category + priority + reply |
| 3 | Few-shot (3 examples) | Same task as Step 2 |

## Results

| Metric | Zero-shot | Few-shot |
| --- | --- | --- |
| Correct category (/12) | 12 | 12 |
| Correct priority (/12) | 12 | 12 |
| Reply follows ChillarPay tone (/12) | 11 | 12 |
| Table format followed (/12) | 12 | 12 |

## Key learnings

1. **Zero-shot is enough for simple tasks:** all 12 summaries were accurate with instructions alone, so examples would only add length and cost.
2. **Few-shot teaches company-specific rules:** it fixed M07, where the zero-shot reply gave a refund timeframe ("a few working days") against the no-refund-date rule.
3. **Hinglish and tricky messages:** M03, M06, M11, M12 (Hinglish) and M08, M09, M10 (tricky) were already handled correctly with zero-shot, so examples did not change them.
4. **Limitation:** few-shot copied the examples' wording (M01) and, like zero-shot, referred to a "Profile > Settings" path that is not in the case, so a human must check replies.

## My recommendation to ChillarPay

Use the few-shot prompt for daily support because its replies followed the tone rules more consistently, and keep a human check on every High-priority ticket. Keep zero-shot for summaries. Re-test on 100+ messages before going live.

## Skills shown

Prompt engineering · Zero-shot and few-shot prompting · Synthetic data creation · AI output evaluation · Customer-support operations · FinTech domain knowledge

## What I learned

- Zero-shot prompting (instructions only) works well for simple, common tasks like summarising.
- Few-shot prompting (instructions + solved examples) teaches AI a company's own rules, tone and format.
- Start with the simplest prompt, and add examples only when the output misses the rules.
- How to create a realistic synthetic dataset with AI, without using real customer data.
- Why the answer key must be written before testing, so AI output is judged fairly.
- How to measure AI quality with a scorecard instead of gut feeling.
- AI output must always be checked by a human before business use.

*ChillarPay and all data in this project are fictional and created for learning.*
