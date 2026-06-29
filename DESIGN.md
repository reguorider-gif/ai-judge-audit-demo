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

2026-06-29 module auto-match note: treat the homepage as Landing/marketing primary and Data-viz/report secondary. The first viewport must explain "risky AI output in, signed audit packet out" before showing multi-seat theater. Use the four product artifacts as the story spine: Radar Card, Problem Contract, Verdict Packet, and Final Report. Finance/investment examples can appear only as secondary cases; the primary buyer path is eval/RAG/agent teams sending one failed or borderline output for review.

2026-06-29 taste-layer validation note: keep the homepage hybrid but state-first. Use Landing/marketing primary with Data-viz/report as the first-viewport proof layer. Effective dials for this demo are `DESIGN_VARIANCE 4`, `MOTION_INTENSITY 2`, and `VISUAL_DENSITY 7`. The first viewport must include a compact verdict panel with decision, claim count, blockers, signer, and evidence rows before the user reaches the deeper OpenCouncil stage. On mobile, order the content as product promise, verdict panel, primary actions, then the four-step flow cards. Visible labels should be Chinese by default; keep English only for technical metadata such as loop IDs, JSON keys, or external tool names. Do not use visible em dashes as copy styling, and do not use `word-break: break-all` for CJK UI text.

2026-06-29 visual system v2 note: AI Judge's durable visual motif is not a generic AI landing page and not a photography-style cinematic template. Treat the homepage as an "AI tribunal": a multi-seat council room, an evidence packet, and a human decision desk. The transferable lesson from garden-skills is the system, not the forest aesthetic: one strong scene, clear metadata labels, real media as proof, restrained motion, and a first viewport that feels authored.

The v2 first screen should combine three product truths:

- **Tribunal room:** multiple AI seats examine the same question independently.
- **Evidence packet:** the answer is decomposed into claims, support, contradictions, and risk.
- **Decision desk:** a human can sign, block, or ask for a safer rewrite.

Use these as reusable modules:

- `Tribunal Stage`: dark product surface, OpenCouncil screenshot, seat rail, verdict sheet, and evidence ticker. The screenshot stays the real proof; overlays explain what AI Judge adds.
- `Evidence Tags`: compact labels such as `CASE ID`, `13 SEATS`, `2 ROUNDS`, `EVIDENCE`, `SIGNER`, and `RISK`. They replace decorative status chips.
- `Case File Cards`: each case reads like a small docket, with domain, question, majority result, dissent or risk, and a final action.
- `Decision Pipeline`: three steps from question intake to independent seats to signable conclusion.

Motion rules for v2: use small pulses for active seats, slow reveal for evidence rows, and a subtle lock-in state for verdict panels. Motion must never hide content for screenshots or slow devices; add a timed fallback when using reveal.

## Component Rules

- Primary CTA: black pill with white text.
- Secondary CTA: white or transparent pill with a hairline border.
- Cards: white surface, 1px hairline border, subtle stacked shadow only when a product mockup needs depth.
- Technical labels: mono uppercase, compact, and used only for metadata, claim IDs, status, and workflow numbers.
- Chinese readability beats density. Keep hero and section headings at line-height 1.12 or above, body copy near 17px with generous line-height, and avoid 10-11px text except for secondary metadata.
- Product mockups: dark audit workspace surfaces with readable evidence rows, compact chips, and tabular numeric metrics.
- Primary visual proof: `assets/openspark-council.png`, framed as an OpenSpark/OpenCouncil roundtable surface with seat count and judge status. Use it to make "agent council loop" concrete before showing deeper report mechanics.
- Hero live mock: overlay the Council screenshot with a restrained "AI Judge lens" and a compact Loop QA Packet preview. The overlay must explain transformation from live council state to packet fields, not behave like decoration.
- V2 product proof: show the Council screenshot as the tribunal room center, then flank it with a seat rail and a verdict sheet. The surrounding UI should say what the system is doing now: seats reviewing, evidence counted, dissent found, human signer pending or ready.

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
- V2 mobile order: promise, primary CTA, tribunal screenshot, verdict sheet, case files, decision pipeline, closing CTA. Do not merely stack desktop columns if labels become unreadable.

## Don't

- Do not add brand-like decorative blobs or unrelated illustration.
- Do not use warm editorial serif moments for verdict text; verdicts should feel operational.
- Do not introduce extra accent colors unless they represent evidence states.
- Do not copy Vercel or Mintlify branding, names, exact gradients, or proprietary fonts.
- Do not copy garden-skills' photography/forest aesthetic. The useful ability is the authored scene and metadata system, not the visual subject.
- Do not let reveal animations leave cards invisible in full-page screenshots or non-scrolled capture.
