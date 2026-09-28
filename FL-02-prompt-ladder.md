# FL-02 — The Prompt Ladder

## Task

Improve my FlyRank case study so it is stronger for an ML internship portfolio.

---

## Baseline — Weak Prompt

### Prompt

Help me improve my FlyRank case study.

### Output

Your FlyRank case study is a good starting point. You could improve it by making the problem clearer, explaining your methodology, highlighting the results, and discussing what you learned. Try to make the writing more concise and focused on your contribution.

### Notes

**What changed:** Nothing was specified beyond improving the case study.

**What improved in the output:** The response identified some general areas that could be improved.

**What still failed:** The advice was generic and did not produce an actual improved case study.

**What I would try next:** Give the prompt a clearer goal.

---

# Version 1 — Clearer Goal

### Layer: Goal

### Prompt

Rewrite my FlyRank case study to make it clearer and more convincing for an ML internship portfolio.

### Output

FlyRank — Content Decline Prioritization

I built a machine-learning solution to help content teams identify which pages were worth investigating or refreshing when search performance declined.

Using anonymized Google Search and engagement data, I created 90-day features and compared recent performance with the previous 45-day period. I trained a Random Forest classifier to rank pages based on their likelihood of meaningful performance decline.

The model achieved 0.680 Precision@50 compared with a 0.380 baseline on the held-out evaluation.

The result was a prioritised list of pages that a content team could investigate first rather than treating every declining page equally.

### Notes

**What changed:** I explicitly stated the goal: make the case study clearer and more convincing for an ML internship portfolio.

**What improved in the output:** The response became more focused and produced an actual rewritten case study instead of only giving general advice.

**What still failed:** It did not explicitly consider who would read the case study.

**What I would try next:** Define the audience.

---

# Version 2 — Defined Audience

### Layer: Audience

### Prompt

Rewrite my FlyRank case study to make it clearer and more convincing for a hiring manager reviewing an ML internship portfolio. Focus on what demonstrates practical machine-learning ability.

### Output

FlyRank — Content Decline Prioritization

### Problem

SEO and content teams manage many pages, but they cannot investigate every page showing declining search performance. I wanted to build a way to prioritize which pages deserved attention first.

### Approach

I worked with anonymized Google Search and engagement data and created features from 90-day performance, including comparisons between the most recent 45 days and the previous 45 days.

I trained a Random Forest classifier to rank pages based on their likelihood of meaningful search-performance decline.

### Result

The model achieved **0.680 Precision@50**, compared with **0.380 for the baseline**, on a held-out evaluation grouped by client.

The output was a prioritized list of pages that could be investigated by a content team.

### Notes

**What changed:** I specified that the audience is an ML internship hiring manager.

**What improved in the output:** The response focused more on the technical work, evaluation, and practical application rather than generic portfolio advice.

**What still failed:** It assumed a structure but did not specify exactly what information should be included.

**What I would try next:** Define the required format.

---

# Version 3 — Specific Output Format

### Layer: Output Format

### Prompt

Rewrite my FlyRank case study for an ML internship hiring manager.

Use exactly these sections:
1. Problem
2. Data
3. Approach
4. Results
5. Practical Use

Keep it under 300 words and focus on my actual machine-learning work.

### Output

## Problem

SEO and content teams manage many pages, but they have limited time to investigate declining pages. I wanted to identify which pages were worth prioritizing for investigation or potential refresh.

## Data

I used the FlyRank/internship-warehouse dataset containing anonymized Google Search and engagement data. I created 90-day features and compared the most recent 45 days with the previous 45 days.

## Approach

I trained a Random Forest classifier using signals including previous-period impressions, visible queries, query-share features, and search-position volatility. I evaluated the model using a held-out split grouped by client.

## Results

The model achieved **0.680 Precision@50**, compared with **0.380 for the baseline**.

## Practical Use

The model produces a prioritized list of pages for a content team to investigate first. It is a prioritization tool rather than an automatic decision to refresh content.

### Notes

**What changed:** I specified the exact sections and a 300-word limit.

**What improved in the output:** The response became structured, concise, and easier for a hiring manager to scan.

**What still failed:** It did not explicitly require the response to distinguish measured results from proposed practical use.

**What I would try next:** Add quality criteria.

---

# Version 4 — Quality Criteria

### Layer: Quality Criteria

### Prompt

Rewrite my FlyRank case study for an ML internship hiring manager.

Use exactly these sections:
1. Problem
2. Data
3. Approach
4. Results
5. Practical Use

Keep it under 300 words.

Quality criteria:
- Be specific about the machine-learning work.
- Include the 0.680 Precision@50 result and 0.380 baseline.
- Do not claim production deployment or real-world impact that was not measured.
- Clearly distinguish what I built from what a content team could potentially do with the output.
- Use natural, direct language with no buzzwords.

### Output

## Problem

SEO and content teams manage many pages, but they have limited time to investigate every page showing declining search performance. I wanted to build a way to prioritize which pages were worth investigating first.

## Data

I used the FlyRank/internship-warehouse dataset containing anonymized Google Search and engagement data. I created 90-day features and compared the most recent 45 days with the previous 45 days.

## Approach

I trained a Random Forest classifier using signals including previous-period impressions, visible queries, query-share features, and search-position volatility. Evaluation used a held-out split grouped by client.

## Results

The model achieved **0.680 Precision@50**, compared with **0.380 for the baseline**.

## Practical Use

The model produces a prioritized list of pages that a content team could investigate first. I did not deploy it to a production content team or measure the effect of actual content refreshes, so I treat it as a prioritization tool rather than evidence of business impact.

### Notes

**What changed:** I added explicit quality criteria, especially around accuracy and avoiding unsupported claims.

**What improved in the output:** The case study became more precise and clearly separated measured model performance from potential practical use.

**What still failed:** The prompt still relied on the model to decide what information was important without giving it the underlying source material.

**What I would try next:** Provide the actual case-study information as source material and require verification against it.

---

# Version 5 — Review / Verification Instructions

### Layer: Review Instructions

### Prompt

Rewrite my FlyRank case study using the source information below.

Audience: ML internship hiring manager.

Use exactly these sections:
1. Problem
2. Data
3. Approach
4. Results
5. Practical Use

Keep it under 300 words.

Quality criteria:
- Be specific about the machine-learning work.
- Include the 0.680 Precision@50 result and 0.380 baseline.
- Do not claim production deployment or real-world impact that was not measured.
- Clearly distinguish measured results from potential use.
- Use natural, direct language with no buzzwords.

Before finalizing, check every factual claim against the source information. If something is not supported, leave it out rather than guessing.

### Source information

I built a Random Forest classifier for FlyRank to prioritize content pages showing search-performance decline.

I used the FlyRank/internship-warehouse dataset containing anonymized Google Search and engagement data.

I created 90-day features and compared the most recent 45 days with the previous 45 days.

Features included previous-period impressions, visible queries, rare-query share, anonymous-query share, top-query share, and search-position volatility.

The model achieved 0.680 Precision@50 compared with a 0.380 baseline.

Evaluation used a held-out split grouped by client.

The output is a prioritization of pages for investigation. The project did not involve production deployment or measuring the effect of actual content refreshes.

### Output

## Problem

SEO and content teams manage many pages, but they have limited time to investigate every page showing declining search performance. I wanted to build a way to prioritize which pages were worth investigating first.

## Data

I used the FlyRank/internship-warehouse dataset containing anonymized Google Search and engagement data. I created 90-day features and compared the most recent 45 days with the previous 45 days.

## Approach

I trained a Random Forest classifier using previous-period impressions, visible queries, query-share signals, and search-position volatility. I evaluated it using a held-out split grouped by client.

## Results

The model achieved **0.680 Precision@50**, compared with **0.380 for the baseline**.

## Practical Use

The output is a prioritized list of pages that a content team could investigate first. The project did not include production deployment or measurement of actual content-refresh impact, so the result demonstrates prioritization rather than proven business impact.

### Notes

**What changed:** I supplied the source information and added a verification instruction requiring every factual claim to be checked against it.

**What improved in the output:** The final version is more accurate, specific, concise, and clearly separates measured results from potential use.

**What still failed:** The case study still does not demonstrate measured real-world impact because that was not part of the project.

**What I would try next:** Create a usable output artifact that shows how the model's ranking could be consumed by a content team.

---

# Final Reusable Prompt

Rewrite the following ML project into a concise portfolio case study for an ML internship hiring manager.

Use these sections:
1. Problem
2. Data
3. Approach
4. Results
5. Practical Use

Keep it under 300 words.

Use direct, natural language with no buzzwords or filler. Focus on the actual machine-learning work and measured results.

Do not invent datasets, metrics, deployment, users, or business impact. Clearly distinguish measured results from potential use.

Before finalizing, check every factual claim against the source information. If a detail is not supported, leave it out rather than guessing.

Source information:
[PASTE PROJECT DETAILS HERE]
