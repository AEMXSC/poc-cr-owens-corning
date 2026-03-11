# AGENTS.md — Multi-Agent Context (Cursor, Codex, Gemini CLI)

# CLAUDE.md — AI Agent Context for Owens Corning POC

## Project Type
This is an **Adobe Experience Manager Edge Delivery Services (EDS)** project.
Reference documentation: https://www.aem.live
LLM-optimized docs: https://www.aem.live/llms.txt

## Key Rules for AI Agents
1. **This is NOT a React/Next.js project.** It uses vanilla JS/CSS with the EDS block decorator pattern.
2. Every block lives in `/blocks/<block-name>/` with a JS file and optional CSS file.
3. Block JS exports a default `decorate(block)` function that receives a `<div>` element.
4. Content comes from Word/Google Docs via Document Authoring (DA) — NOT from a CMS database.
5. DO NOT use npm, webpack, or any build tools. Scripts load via `/scripts/scripts.js`.
6. CSS uses vanilla CSS custom properties. NO Tailwind, NO SASS.

## Block Decorator Pattern
```js
export default function decorate(block) {
  // block is a <div> with class matching the block name
  // Rows = block.children, Cells = row.children
  const rows = [...block.children];
  rows.forEach((row) => {
    const cols = [...row.children];
    // Transform DOM here
  });
}
```

## Customer Context
- **Customer**: Owens Corning
- **Vertical**: Manufacturing
- **DR#**: TBD
- **Demo Moments**: EDS Performance & Authoring Speed, AI-Powered Content & Asset Creation, Seamless Cross-Channel Content Delivery, Personalization & Experimentation, Integrated DAM & Authoring Experience

## Blocks in This Repo
- `/blocks/hero-image-carousel/`
- `/blocks/fragment/`
- `/blocks/embed/`
- `/blocks/aicards/`
- `/blocks/cards/`
- `/blocks/cards/`
- `/blocks/card/`
- `/blocks/aicarousel/`
- `/blocks/carousel/`

## Brand & Design
- Brand CSS is in `/styles/brand.css`
- Customer colors and fonts are defined as CSS custom properties
- All block CSS should use `var(--color-brand-*)` tokens for theming

## What NOT to Do
- Do NOT generate React components
- Do NOT use `import` for CSS (use `<link>` or CSS loaded by scripts.js)
- Do NOT create package.json or node_modules
- Do NOT modify /scripts/aem.js (it's the EDS runtime)


## Additional Agent Instructions
- When asked to "create a block", always scaffold in /blocks/<name>/<name>.js + <name>.css
- Test blocks by previewing at https://main--poc-cr-owens-corning--aemxsc.aem.live
- Use https://www.aem.live/developer/block-collection for reference implementations
