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
    fontFamily: "Inter, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "64px"
    fontWeight: 650
    lineHeight: 0.98
    letterSpacing: "0"
  body:
    fontFamily: "Inter, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.62
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

## Component Rules

- Primary CTA: black pill with white text.
- Secondary CTA: white or transparent pill with a hairline border.
- Cards: white surface, 1px hairline border, subtle stacked shadow only when a product mockup needs depth.
- Technical labels: mono uppercase, compact, and used only for metadata, claim IDs, status, and workflow numbers.
- Product mockups: dark audit workspace surfaces with readable evidence rows, compact chips, and tabular numeric metrics.

## Layout Rules

- Keep the hero split: product promise on the left, Loop QA packet preview on the right.
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
