---
version: alpha
name: ai-judge-audit-demo-design
description: Visual rules for AI Judge, a source-isolated audit packet layer for LLM evaluation and RAG trace review.

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
    letterSpacing: "-0.045em"
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
    letterSpacing: "0.08em"

rounded:
  sm: "6px"
  md: "10px"
  lg: "16px"
  xl: "22px"
  pill: "9999px"
---

## Overview

AI Judge should feel like a precise review workspace for eval, RAG, and observability teams. The page should communicate trust, evidence handling, and reviewer handoff before it tries to feel expressive.

## Design Direction

Use Vercel-like black/white precision for the developer-platform layer and Mintlify-like documentation rhythm for the audit-packet reading layer. Keep the palette mostly monochrome; reserve the green accent for evidence, source support, and active review signals.

## Component Rules

- Primary CTA: black pill with white text.
- Secondary CTA: white or transparent pill with a hairline border.
- Cards: white surface, 1px hairline border, subtle stacked shadow only when a product mockup needs depth.
- Technical labels: mono uppercase, compact, and used only for metadata, claim IDs, status, and workflow numbers.
- Product mockups: dark audit workspace surfaces with readable evidence rows, compact chips, and tabular numeric metrics.

## Layout Rules

- Keep the hero split: product promise on the left, audit packet preview on the right.
- Favor tight internal rhythm inside cards and generous spacing between major sections.
- Use table-like rows for integrations and fit statements, not decorative feature cards.
- On mobile, protect touch targets and hide only secondary mockup details, never the core claim/verdict.

## Don't

- Do not add brand-like decorative blobs or unrelated illustration.
- Do not use warm editorial serif moments for verdict text; verdicts should feel operational.
- Do not introduce extra accent colors unless they represent evidence states.
- Do not copy Vercel or Mintlify branding, names, exact gradients, or proprietary fonts.
