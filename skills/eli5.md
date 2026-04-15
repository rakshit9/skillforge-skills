---
name: eli5
description: |
  Explain Like I'm 5. Breaks down any complex topic into simple, clear language
  that anyone can understand — without dumbing it down.
  Use when: "explain this simply", "ELI5", "what does this mean",
  "explain like I'm not technical", "break this down".
---

# ELI5 · Explanation Skill

> "If you can't explain it simply, you don't understand it well enough." — Einstein

## When to Activate

Use this skill when the user wants something explained simply:
- "Explain this like I'm 5"
- "ELI5"
- "What does [concept] actually mean?"
- "Explain this without jargon"
- "I don't have a technical background — explain this to me"

**Exit**: user says "exit" or "I get it"

## Core Approach

### 1. Find the Simplest True Analogy
The best explanation is one that:
- Uses something the person already knows
- Captures the essential mechanism (not just the surface similarity)
- Doesn't require any background knowledge

Bad analogy: "Blockchain is like a spreadsheet" (too vague)
Good analogy: "Blockchain is like a notebook that 1000 people have identical copies of — if you change your copy, everyone else can see it doesn't match theirs"

### 2. Build Up Layer by Layer
Start with the simplest version that is still true.
Add complexity only when the simple version is understood.

Never skip to the advanced explanation before the simple one lands.

### 3. Use Concrete Numbers and Examples
❌ "It processes transactions very quickly"
✅ "It processes 100,000 transactions per second — that's like processing every transaction in a football stadium simultaneously"

### 4. Check Understanding
After explaining, ask: "Does that make sense, or should I try a different angle?"

## Explanation Templates

### For Concepts
```
SIMPLE VERSION (one sentence)
[What it is in plain language]

WHY IT EXISTS
[The problem it solves]

ANALOGY
[Real-world comparison that captures the mechanism]

EXAMPLE
[Concrete instance everyone can relate to]

THE ONE THING TO REMEMBER
[The most important takeaway]
```

### For Processes
```
WHAT IT DOES (outcome)
[What happens as a result]

HOW IT WORKS (step by step)
1. [First thing that happens]
2. [Second thing]
3. [Result]

ANALOGY
[Like [familiar process], except...]
```

### For Technical Terms
```
PLAIN ENGLISH
[No jargon version]

WHY ENGINEERS CALL IT "[TERM]"
[Where the word comes from]

WHEN YOU'D ENCOUNTER THIS
[Real situation where this matters]
```

## Common Explanations (Examples)

**API**: A waiter at a restaurant. You (the app) tell the waiter (API) what you want. The waiter goes to the kitchen (the server), gets it, and brings it back to you. You never go into the kitchen directly.

**Machine Learning**: Teaching a child to recognize cats by showing them 10,000 pictures of cats and dogs, saying "cat" or "not cat" each time. Eventually they can identify a cat they've never seen before. ML models learn the same way — from millions of examples.

**DNS**: The internet's phonebook. You remember "google.com" (a name), but computers only understand numbers (IP addresses). DNS translates the name into the number — just like a phonebook translates "John Smith" into his phone number.

**Encryption**: A lock-and-key system where the key is a huge number. Only someone with the right key can unlock (read) the message. Even if someone intercepts the locked message, they can't read it.

**Recursion**: A mirror facing a mirror. The reflection contains another reflection, which contains another, and so on. In code, a function that calls itself — each call is a smaller version of the same problem.

## What Not to Do

- ❌ Use jargon and then explain the jargon with more jargon
- ❌ Add so many caveats that the simple explanation disappears
- ❌ Condescend — simple ≠ stupid
- ❌ Oversimplify to the point of being wrong
- ❌ Give multiple analogies at once — pick the best one

## Calibrating Complexity

Ask if unsure: "How familiar are you with [related concept]?"

Then adjust:
- **No background**: Pure analogy, no technical terms at all
- **Some background**: One technical term, immediately explained
- **Moderate background**: Standard explanation with one analogy for the tricky part
- **Technical background**: Skip to the nuance they're actually missing

## Honest Limits

- Some concepts genuinely require prerequisites — flag when this is the case
- Analogies always break down somewhere — be explicit about where the analogy stops working
- "Simple" and "complete" are in tension — ELI5 prioritizes understanding over completeness
