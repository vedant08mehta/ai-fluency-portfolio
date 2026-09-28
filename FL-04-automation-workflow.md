# FL-04 — Ship an Automation Workflow v2

## Workflow

### Task

Automate part of my internship application workflow by turning a job description into a tailored application response.

### Pipeline

Job Description
→ Draft
→ Critique
→ Revised Response

### Why I chose this

Internship applications were one of my FL-01 focus tasks. I repeatedly need to understand a job description, write a tailored response, check it for weaknesses, and revise it. Chaining these steps together makes the process more repeatable while keeping a human review at the end.

---

## Step 1 — Draft

### Input

A real internship/job description.

### Prompt

Read this job description and draft a concise, truthful application response tailored to the role.

Use only information provided about the candidate.

Do not invent skills, experience, metrics, qualifications, or projects.

---

## Step 2 — Critique

### Input

The job description + draft from Step 1.

### Prompt

Critique this application response for:

1. Relevance to the job description
2. Clarity
3. Specificity
4. Unsupported or exaggerated claims
5. Missing important information

For each issue, explain the specific change that should be made.

---

## Step 3 — Revise

### Input

The job description + original draft + critique.

### Prompt

Rewrite the application response using the critique.

Keep it concise, natural, and specific to the role.

Preserve factual information.

Do not invent skills, experience, metrics, qualifications, or projects.

Return only the revised application response.

---

## Human Review

The final output is not submitted automatically.

I review the final response before using it in an application, checking:

- Whether every claim is true
- Whether the response actually matches the job
- Whether anything important was omitted
- Whether the writing sounds like me
- Whether any AI-generated wording needs editing

---

## Known Failure Points

1. The system may produce generic language if the job description is vague.
2. The model may emphasize a requirement that is not actually important to the role.
3. It may produce wording that sounds too polished or unnatural.
4. It could make unsupported assumptions about my experience.
5. A human must verify the final response before it is submitted.

---

## Five-Run Log

| Run | Input | Result | Time |
|---|---|---|---|
| 1 | [Job description] | [Result] | [Time] |
| 2 | [Job description] | [Result] | [Time] |
| 3 | [Job description] | [Result] | [Time] |
| 4 | [Job description] | [Result] | [Time] |
| 5 | [Job description] | [Result] | [Time] |

---

## Manual vs Automated

### Manual process

I would normally read the job description, draft a response, reread it for problems, and rewrite it.

Estimated manual time: approximately 15–20 minutes per application.

### Automated workflow

The workflow chains drafting, critique, and revision into one repeatable process.

Actual automated time will be recorded during the five test runs.

The workflow does not remove the final human review.

---

## Handoff Points

1. Job description → Drafting AI
2. Draft → Critique AI
3. Draft + Critique → Revision AI
4. Revised response → Human review

---

## Workflow Limitations

The workflow improves consistency and reduces repetitive writing work, but it does not make the final application decision.

Human review remains necessary because the AI can misunderstand requirements or produce claims that need correction.
