# FL-04 — Three Roads: Choose Your Stack with AI

## My Constraints

### Cost
The portfolio must be free to build and host.

### My skill level
I am comfortable with Python and basic web development, but I want to avoid unnecessary complexity for a portfolio project.

### What the portfolio needs to do
The portfolio needs to:
- Present my one-line claim clearly.
- Display three case studies.
- Show real project screenshots.
- Include my identity kit and consistent visual style.
- Link to GitHub repositories and my resume.
- Provide a clear contact CTA.
- Work well on desktop and mobile.

### How the work must be displayed
The portfolio mainly needs text, images/screenshots, links, and case studies. It does not currently require a complex backend or dynamic application.

### Backend requirement
**No backend is required for the initial portfolio.**

---

# Three Stack Options

## Option 1 — Static HTML + CSS + GitHub Pages

### How I would build it
Create the portfolio using HTML and CSS, with images and content stored directly in the repository.

### Hosting
GitHub Pages.

### Backend
None.

### Trade-off
This is the simplest option and is completely free, but I would need to manage the HTML/CSS manually as the portfolio grows.

---

## Option 2 — React + Vite + GitHub Pages

### How I would build it
Use React with Vite to create reusable components for the Home, Case Studies, About, and Contact sections.

### Hosting
GitHub Pages or another free static host.

### Backend
None required.

### Trade-off
It provides a cleaner component structure and makes future changes easier, but it adds setup and complexity that the current portfolio does not really require.

---

## Option 3 — Next.js + Tailwind CSS + Vercel

### How I would build it
Use Next.js with Tailwind CSS and deploy it through Vercel.

### Hosting
Vercel free tier.

### Backend
Not required for the current portfolio, although Next.js gives the option to add server-side functionality later.

### Trade-off
This is the most powerful and flexible option, but it introduces more framework complexity and setup than I need for a portfolio that is primarily static content.

---

# Pressure Test

### If I choose the simplest option

I can finish the basic portfolio quickly and host it for free. It can display my case studies, screenshots, resume, GitHub links, and contact information without needing a backend.

The main trade-off is that maintaining many pages or interactive components manually would become less convenient.

### If I choose the most powerful option

Next.js would give me more flexibility for future features, but I would spend more time managing framework and deployment complexity that does not directly improve the current portfolio.

### Can I maintain it?

Yes. I can maintain a static HTML/CSS portfolio because the structure and technologies are straightforward.

### Can I finish it in two weeks?

Yes. A static portfolio can realistically be completed within two weeks without requiring unnecessary infrastructure.

### Does it show my work properly?

Yes. A static site can display case studies, screenshots, project links, charts, and other evidence of my work.

---

# My Decision

## Chosen Stack: HTML + CSS + GitHub Pages

I chose a static HTML/CSS site hosted on GitHub Pages.

I chose it because my portfolio is primarily a collection of case studies, screenshots, links, and written content. It does not currently need a backend or complex application logic.

The biggest advantage is that it is **free, simple to maintain, easy to deploy, and sufficient for displaying my work properly**.

I would rather spend the available time improving the actual case studies and presentation than adding framework complexity that does not improve what a visitor needs to see.

### Alternatives I considered

1. **React + Vite** — better component structure, but more complexity than I currently need.
2. **Next.js + Tailwind + Vercel** — more powerful and extensible, but unnecessary for the current portfolio.

### Can I maintain this?

**Yes.** The stack is simple enough for me to understand and maintain myself.

### Does it show my work well?

**Yes.** It supports the screenshots, case studies, links, resume, and CTA that my content map requires.
