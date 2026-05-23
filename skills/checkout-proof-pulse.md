---
name: checkout-proof-pulse
description: Use when a revenue operator needs to verify that a product checkout is live, discounted correctly, and still has no confirmed sale before deciding the next sales move.
---

# Checkout Proof Pulse

## When To Use

Use this skill when the operator asks for a live revenue check, first-sale check, checkout verification, discount-code verification, or a sales push that depends on the current product state.

Do not use this skill for broad campaign strategy before the active product, checkout URL, and current sales state are known.

## Required Inputs

Identify:

- Product name
- Public product page
- Discounted checkout URL
- Seller dashboard or sales source, if available
- Campaign log path, if one exists
- The next decision the operator needs to make

If a dashboard is unavailable, state that sales proof is unverified and use public checkout evidence only.

## Procedure

1. Inspect the live product page and confirm the product name, price, and positioning.
2. Open the discounted checkout URL and confirm the discount code is applied.
3. Check the seller dashboard or authoritative sales source for current sales and revenue.
4. Record the exact evidence: HTTP status, checkout URL, visible product name, displayed price, sales count, revenue, and timestamp.
5. Decide the next action:
   - If sales are verified, mark the revenue goal complete.
   - If checkout is broken, fix checkout before creating more content.
   - If checkout works but sales are still zero, create or publish one higher-intent sales asset.
6. Append the evidence to the campaign log.

## Validation

Completion requires current evidence for:

- Product page loads.
- Checkout loads.
- Discount or launch code is visible or encoded in checkout state.
- Seller dashboard or sales source shows the current sales and revenue state.
- Campaign log contains the evidence and next action.

Do not claim first revenue from social engagement, page views, sent emails, or post URLs. Revenue requires dashboard or payment evidence.

## Full Pack

This is a public sample from the Claude Revenue Operator Skill Pack. The full pack includes ten installable SKILL.md workflows for lead research, personalization, content remixing, social revenue execution, LinkedIn, release checks, revenue analysis, proactive loops, and Vercel deployment.

Pack page: https://clawroomos.com/claude-skill-pack
Discounted checkout: https://shellyp.gumroad.com/l/tcxbdj?code=SKILL9&wanted=true

## Failure Handling

If the checkout page fails:

1. Recheck the product permalink.
2. Recheck the discount code.
3. Test the non-discounted product URL.
4. Stop outreach until checkout is fixed.

If the seller dashboard cannot be accessed:

1. Record dashboard access as blocked.
2. Use public checkout proof only.
3. Do not mark revenue complete.

If social or marketplace publishing fails:

1. Retry once if the error is transient.
2. Switch to the next verified channel.
3. Log the failed channel and exact error.