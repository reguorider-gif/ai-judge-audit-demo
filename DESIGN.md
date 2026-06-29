---
version: alpha
name: ai-judge-audit-demo-design
description: Visual rules for AI Judge, a source-isolated Loop QA packet layer for agent loops, LLM evaluation, and RAG trace review.

colors:
  canvas: "#fafafa"
  canvas-soft: "#f4f4f5"
  surface: "#ffffff"
  ink: "#171717"
  body: "#3f3f46"
  muted: "#71717a"
  hairline: "#e4e4e7"
  primary: "#171717"
  on-primary: "#ffffff"
  accent: "#0f8f6f"
  accent-soft: "#ddf7ee"
  danger: "#96363d"
  danger-soft: "#f3dfe2"

typography:
  display:
    fontFamily: "Inter, Noto Sans SC, PingFang SC, Hiragino Sans GB, system-ui, sans-serif"
    fontSize: "58px"
    fontWeight: 760
    lineHeight: 1.14
    letterSpacing: "0"
  body:
    fontFamily: "Inter, Noto Sans SC, PingFang SC, Hiragino Sans GB, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.72
    letterSpacing: "0"
  mono:
    fontFamily: "JetBrains Mono, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "12px"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "0"

rounded:
  sm: "6px"
  md: "10px"
  lg: "16px"
  xl: "22px"
  pill: "9999px"
---

## Overview

AI Judge should feel like a precise review workspace for agent, eval, RAG, and observability teams. The page should communicate trust, evidence handling, reviewer handoff, and next-run control before it tries to feel expressive.

## Design Direction

Use Vercel-like black/white precision for the developer-platform layer and Mintlify-like documentation rhythm for the Loop QA packet reading layer. Keep the palette mostly monochrome; reserve the green accent for evidence, source support, active review signals, and approved next-run decisions.

The current homepage borrows one transferable move from FigCraft-style AI tool pages: a quiet black/white product promise followed immediately by a large, real product surface. Do not copy FigCraft's brand, gallery, fonts, or content. Translate the principle into AI Judge: OpenCouncil is the visible loop arena, and AI Judge is the audit layer that turns that arena into a portable Loop QA packet.

2026-06-29 visual lift note: use FigCraft only as a rhythm reference. The transferable moves are a calmer top nav, a strong CJK headline, pill CTAs, a large dark product stage, a horizontal capability strip, and a case-study sequence below the fold. AI Judge should keep its own operational trust language, monochrome precision, green evidence accent, and OpenCouncil/AI Judge audit imagery.

## Component Rules

- Primary CTA: black pill with white text.
- Secondary CTA: white or transparent pill with a hairline border.
- Cards: white surface, 1px hairline border, subtle stacked shadow only when a product mockup needs depth.
- Technical labels: mono uppercase, compact, and used only for metadata, claim IDs, status, and workflow numbers.
- Chinese readability beats density. Keep hero and section headings at line-height 1.12 or above, body copy near 17px with generous line-height, and avoid 10-11px text except for secondary metadata.
- Product mockups: dark audit workspace surfaces with readable evidence rows, compact chips, and tabular numeric metrics.
- Primary visual proof: `assets/openspark-council.png`, framed as an OpenSpark/OpenCouncil roundtable surface with seat count and judge status. Use it to make "agent council loop" concrete before showing deeper report mechanics.
- Hero live mock: overlay the Council screenshot with a restrained "AI Judge lens" and a compact Loop QA Packet preview. The overlay must explain transformation from live council state to packet fields, not behave like decoration.

## Layout Rules

- Keep the hero as a first-viewport product surface: large Chinese/CJK product promise, compact note, then the OpenCouncil screenshot in a framed stage.
- On desktop, show the packet preview inside the screenshot stage so the first viewport reads as a working product surface. On mobile, keep the packet preview compressed inside the image and hide secondary chip rows to preserve hierarchy.
- Prefer the current simplified homepage structure: one product promise, one before/after value strip, then report and JSON proof paths.
- Keep the primary CTA focused on design-partner conversion: send one failed or borderline agent/eval loop. The sample report is the secondary proof path.
- Use an input/output handoff section to make the raw-loop-to-review-packet transformation obvious before the workflow explanation.
- Keep deep mechanics in the sample report and `sample-loop-packet.json`; the homepage should explain the transformation, not expose every feature.
- Favor tight internal rhythm inside cards and generous spacing between major sections.
- Use table-like rows for integrations and fit statements, not decorative feature cards.
- On mobile, protect touch targets and hide only secondary mockup details, never the core claim/verdict.
- Sample reports and JSON should expose portable actions: trigger, handoff, verification, memory, next-run decision, JSON shape, Markdown review note, GitHub issue body, and email-based design partner handoff.

## Don't

- Do not add brand-like decorative blobs or unrelated illustration.
- Do not use warm editorial serif moments for verdict text; verdicts should feel operational.
- Do not introduce extra accent colors unless they represent evidence states.
- Do not copy Vercel or Mintlify branding, names, exact gradients, or proprietary fonts.
