# FL-02 — Prompting Fundamentals on Real Tasks v2

## Real Task

**FL-01 focus task:** Internship applications

### Specific task
Tailor my resume for an AI/ML internship.

---

# Version 0 — Naive Prompt

### Technique
Baseline / no engineered technique

### Prompt

Tailor my resume for an AI/ML internship.

### Output

Your resume should emphasize your machine-learning experience, Python skills, relevant projects, and technical skills. You should highlight your internship experience and projects involving machine learning, data analysis, and Python.

### What changed

This is the original one-line prompt I would have used before learning prompt engineering.

### What improved in the output

It identified some relevant areas of my background.

### What still failed

The response was generic and did not have enough information about my background, target role, or the exact type of output I wanted.

### Next

Add a clear role for the AI.

---

# Version 1 — Role Assignment

### Technique
Role assignment

### Prompt

Act as an experienced recruiter hiring entry-level AI/ML interns.

Tailor my resume for an AI/ML internship.

### Output

Focus the resume on practical machine-learning experience, Python, relevant ML libraries, projects, and measurable results. Emphasize experience that demonstrates the ability to work with real-world data and build machine-learning solutions. Reduce attention on unrelated experience.

### What changed

I assigned the AI the role of an experienced AI/ML recruiter.

### What improved in the output

The response became more focused on what a recruiter would look for in an entry-level AI/ML candidate instead of giving completely general resume advice.

### What still failed

The AI still did not know enough about my background, the type of roles I want, or why I am tailoring the resume.

### Next

Add context and motivation.

---

# Version 2 — Context + Motivation

### Technique
Context and motivation

### Prompt

Act as an experienced recruiter hiring entry-level AI/ML interns.

I am a B.Tech CSE student specializing in AI/ML. I am applying for AI/ML internships and want my resume to demonstrate practical machine-learning ability. I have completed an ML internship and several ML/data projects.

My goal is to make the resume more relevant to AI/ML internship roles while keeping everything truthful. Do not add skills, experience, or results that I do not have.

Tailor my resume for an AI/ML internship.

### Output

The response focuses more strongly on practical ML experience and suggests emphasizing the FlyRank machine-learning internship, relevant projects, Python/ML tooling, and measurable project results. It also avoids recommending unsupported experience.

### What changed

I added information about my education, target role, existing experience, and the reason for tailoring the resume.

### What improved in the output

The advice became more relevant to my actual situation and focused on proving practical ML ability rather than simply listing technical skills.

### What still failed

The response still did not know exactly what strong resume bullets should look like or what format I wanted the output in.

### Next

Give examples of the style I want.

---

# Version 3 — Few-Shot Examples

### Technique
Few-shot examples

### Prompt

Act as an experienced recruiter hiring entry-level AI/ML interns.

I am a B.Tech CSE student specializing in AI/ML. I am applying for AI/ML internships and want my resume to demonstrate practical machine-learning ability. I have completed an ML internship and several ML/data projects.

My goal is to make the resume more relevant to AI/ML internship roles while keeping everything truthful. Do not add skills, experience, or results that I do not have.

Use these examples as a guide for the writing style:

Weak:
"Worked on a machine learning project using Python."

Better:
"Built a Random Forest classifier in Python and evaluated it using Precision@50."

Weak:
"Made an emotion detection application."

Better:
"Built a Streamlit application integrating DeepFace for facial emotion recognition and music recommendations."

Now tailor my resume for an AI/ML internship using this style.

### Output

The response produces more specific, action-oriented suggestions. It emphasizes what was built, the technologies used, and measurable results instead of vague statements such as "worked on" or "learned."

### What changed

I provided examples showing the difference between weak and stronger resume bullets.

### What improved in the output

The suggested wording became more concrete and closer to the style I want to use in my resume.

### What still failed

The output was still not organized in a way that made it easy to apply each recommendation directly to my resume.

### Next

Specify the output structure.

---

# Version 4 — Output Structure

### Technique
Output structure

### Prompt

Act as an experienced recruiter hiring entry-level AI/ML interns.

I am a B.Tech CSE student specializing in AI/ML. I am applying for AI/ML internships and want my resume to demonstrate practical machine-learning ability. I have completed an ML internship and several ML/data projects.

My goal is to make the resume more relevant to AI/ML internship roles while keeping everything truthful. Do not add skills, experience, or results that I do not have.

Use these examples as a guide for the writing style:

Weak:
"Worked on a machine learning project using Python."

Better:
"Built a Random Forest classifier in Python and evaluated it using Precision@50."

Weak:
"Made an emotion detection application."

Better:
"Built a Streamlit application integrating DeepFace for facial emotion recognition and music recommendations."

For every recommended change, use this format:

**Current:**  
[existing content]

**Suggested:**  
[rewritten content]

**Why:**  
[short explanation]

Only suggest changes that materially improve the resume for an AI/ML internship.

### Output

The response now organizes each recommendation into Current, Suggested, and Why sections. This makes the feedback easier to review and apply directly.

### What changed

I specified exactly how the response should be structured.

### What improved in the output

The output became much easier to use because each recommendation clearly separates the original wording, proposed change, and reason for the change.

### What still failed

The AI could still make unnecessary changes instead of reviewing the resume systematically from beginning to end.

### Next

Break the review into explicit steps.

---

# Version 5 — Step Decomposition

### Technique
Step decomposition

### Prompt

Act as an experienced recruiter hiring entry-level AI/ML interns.

I am a B.Tech CSE student specializing in AI/ML. I am applying for AI/ML internships and want my resume to demonstrate practical machine-learning ability. I have completed an ML internship and several ML/data projects.

My goal is to make the resume more relevant to AI/ML internship roles while keeping everything truthful. Do not add skills, experience, or results that I do not have.

Use these examples as a guide for the writing style:

Weak:
"Worked on a machine learning project using Python."

Better:
"Built a Random Forest classifier in Python and evaluated it using Precision@50."

Weak:
"Made an emotion detection application."

Better:
"Built a Streamlit application integrating DeepFace for facial emotion recognition and music recommendations."

Review the resume in these steps:

1. Identify the sections most relevant to an AI/ML internship.
2. Identify weak, vague, repetitive, or irrelevant content.
3. Identify the strongest evidence of practical ML ability.
4. Rewrite only the content that would materially benefit from improvement.
5. Preserve all real metrics, technologies, and experience.
6. Do not invent skills, results, deployment, users, or experience.
7. Present every proposed change as:
   - Current
   - Suggested
   - Why
8. Finish with the five most important changes I should make.

Keep the language concise, natural, technical, and suitable for an internship resume.

### Output

The response now follows a systematic review process. It identifies relevant sections, finds weak or repetitive content, prioritizes practical ML evidence, and then provides targeted rewrites rather than rewriting everything indiscriminately.

### What changed

I broke the task into explicit steps so the AI had a clear process to follow.

### What improved in the output

The final output was more controlled and useful. It focused on the strongest evidence for an AI/ML role and reduced unnecessary rewriting.

### What still failed

The final prompt would work better with the actual job description because different AI/ML internships can prioritize different skills.

### Next

For an actual application, provide the specific internship job description along with the resume.

---

# Final Reusable Prompt Template

```text
Act as an experienced recruiter hiring for [TARGET ROLE].

I am a [BACKGROUND] applying for [TARGET ROLE].
My goal is [GOAL].

Do not invent skills, experience, results, deployment, users, or qualifications.

Use these examples as a guide for the writing style:

[FEW-SHOT EXAMPLES]

Review the material in these steps:

1. Identify the sections most relevant to the target role.
2. Identify weak, vague, repetitive, or irrelevant content.
3. Identify the strongest evidence supporting my fit for the role.
4. Rewrite only content that would materially benefit from improvement.
5. Preserve all factual information and metrics.
6. For every proposed change, provide:
   - Current
   - Suggested
   - Why
7. Finish with the five most important changes.

Keep the language concise, natural, and specific to the target role.
Do not add filler or unsupported claims.

Source material:
[PASTE RESUME / JOB DESCRIPTION / OTHER MATERIAL HERE]
