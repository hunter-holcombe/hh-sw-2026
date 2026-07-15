# Cohere Work-Samples Portfolio — Build Spec & Clip Guide

*Working doc for building the portfolio page. Written so any model (Opus, Fable, etc.) can build it without the original conversation.*

---

## 1. Purpose & context (read first)

- **What this is:** a small set of work samples **requested by Aidan Gomez (CEO/cofounder of Cohere) after Hunter's interview.** He asked to see examples of the work Hunter produces, and wants the rest of the loop to see them too.
- **Audience:** Aidan + the interview loop (Joelle Pineau, Nick Frosst, AJ [Government Affairs], and the Comms interviewer).
- **Intent:** show clean examples of the work. **This is NOT a pitch or a positioning deck.** It's "here are some clips."
- **Register — critical:** *show, don't tell.* Confident restraint. The range and quality of the work imply that Hunter operates at a strategic/systems level **on their own** — do not assert it. No manifesto, no "strategy / my role" breakdowns, no case-study essays. Over-framing reads as trying too hard. The deeper strategic case belongs in live conversation, not on this page.

---

## 2. Framing rules (for whoever writes/builds)

- **One short, plain caption per clip** — what it is + the kind of work. Nothing more.
- Use quiet ownership verbs where true ("I produce," "I run") — they signal ownership as *fact*, not pitch.
- No per-clip strategy explanations. No metrics unless a number is a natural one-liner.
- Minimal, modern, understated aesthetic. **The work dominates; the design gets out of the way.**
- Optional single casual intro line (below). Everything else is just clips + captions.

### Optional intro line (casual — use if a short intro is wanted)
> "Here are a handful of examples across the kinds of work I do — founder thought leadership, event capture, produced explainers, and a podcast I run. Happy to walk through any of them."

---

## 3. Final asset list — 10 clips + 1 written piece

Paths are relative to the Cohere working folder: `/Users/hunterholcombe/Desktop/cohere/`

| # | Caption (use verbatim) | File | Orientation | Quality |
|---|---|---|---|---|
| 1 | **CEO-led explainer (Henry Ward / Carta's ERP vision).** | `portfolio_assets/01_Henry_ERP-explainer_YT.mp4` | Landscape 16:9 | HD 1080p ✅ |
| 2 | **Brand documentary (Google) — longer-form produced piece.** | `portfolio_assets/02_Google_documentary_YT.mp4` | Landscape 16:9 | HD 1080p ✅ |
| 3 | **Henry Ward founder thought leadership, captured on location in DC (equity in 401ks).** | `COHERE EXAMPLES HTML/drive-download-20260702T200142Z-3-001/Henry_401k policy meetings recap_short_FINAL.mp4` | Vertical 9:16 | HD master ✅ |
| 4 | **Event stage capture (Henry Ward, fireside).** | `portfolio_assets/09_Henry_StageCapture-AI_LI.mp4` | Vertical 9:16 | Soft — re-cap at 1080 later |
| 5 | **Interview capture (Henry Ward, HumanX).** | `portfolio_assets/05_Henry_HumanX-capture_LI.mp4` | Vertical 9:16 | Soft — re-cap at 1080 later |
| 6 | **Short-form founder thought leadership (Henry Ward).** | `portfolio_assets/07_Henry_ProductMgmt-TL_LI.mp4` | Vertical 9:16 | Soft — re-cap at 1080 later |
| 7 | **Social thought leadership, "three takeaways" format (Peter Walker).** | `COHERE EXAMPLES HTML/drive-download-20260702T200142Z-3-001/Peter v2 w- graphics.mp4` | Vertical 9:16 | HD master ✅ |
| 8 | **Executive field piece (Charly Kevers, CFO, at SuperReturn).** | `portfolio_assets/04_Charly_BTS_YTshort.mp4` | Vertical 9:16 | Low-res 480p — re-cap recommended |
| 9 | **Data Minute — a recurring podcast I produce with Peter Walker.** | `portfolio_assets/11_DataMinute-2_LI.mp4` | Vertical 9:16 | Soft — re-cap at 1080 later |
| 10 | **Product explainer / demo.** | `portfolio_assets/08_Henry_ProductDemo_LI.mp4` | Landscape 16:9 | Soft — re-cap at 1080 later |
| 11 | **Written thought leadership — ghostwritten for Henry Ward's LinkedIn** ("Looking Back, To Look Forward: An ERP Evolution"). | text (full copy in the source Google Doc) | text | — |

**Quality note:** Items 1, 2, 3, 7 are true HD and carry the page. The soft items (4, 5, 6, 9, 10) are LinkedIn-sourced and compression-capped; item 8 is 480p. Hunter can screen-capture the soft ones at 1080 later — current files are fine as placeholders while building.

---

## 4. Recommended display order (flexible)

Leads with produced HD pieces, groups the Henry founder-brand work, then other leaders/formats, demo last:

1. CEO-led explainer (Henry ERP) — landscape HD
2. Brand documentary (Google) — landscape HD
3. Henry field thought leadership (DC 401k) — vertical HD
4. Henry stage capture (fireside)
5. Henry interview capture (HumanX)
6. Henry short-form thought leadership
7. Peter "three takeaways"
8. Charly Kevers / CFO field piece
9. Data Minute podcast
10. Product explainer / demo
11. Written essay (text block at the end)

---

## 5. Layout & design directions

- **Single self-contained HTML page.** Minimal, understated, modern. Neutral background (a clean near-black like `#0b0b0c` makes video pop; light is also fine). Generous whitespace. Centered content column, max-width ~1100–1200px.
- **Optional intro line** at the top (section 2), small and quiet. No big headline/hero pitch.
- **Handle both orientations** (3 landscape, 7 vertical). Suggested approach: landscape clips can span wider (full column or 2-up); vertical clips sit in a responsive 2–3 up grid. A flex/grid that sizes each card to its aspect ratio works well.
- **Each clip = one card:** the video player + one caption line beneath in small, muted text. No heavy chrome, no numbers, no badges.
- **Playback:** `<video controls playsinline preload="metadata">`. **No autoplay.** Click to play, with sound. Optional poster frame.
- **Written essay:** simple text block (or a lightweight expand/collapse) at the end, under its caption.
- **Responsive:** works cleanly on desktop and mobile.
- **No external dependencies** if avoidable (inline CSS, no frameworks) so the file is portable and openable locally.

---

## 6. Video hosting — two modes

- **Mode A — local review (build first):** reference the local file paths in section 3 directly (`<video src="...">`). Lets Hunter open the page offline, full quality, to review structure. Use relative paths if the HTML file sits in the Cohere folder.
- **Mode B — sharing (final):** upload the chosen clips to **Vimeo (unlisted)** — clean, professional, no clutter, password-optional — and swap each `<video>` for the embed. (The two YouTube-sourced pieces, #1 and #2, can alternatively stay as native YouTube embeds at full quality.) Build so swapping local paths → embed URLs is a one-line change per clip.

---

## 7. Instructions for the builder model

> Build a single self-contained HTML file that presents the 10 clips + 1 written piece from section 3, in the order in section 4, following the design in section 5. Use the **verbatim captions** from the section-3 table (one line under each video). Use the **local file paths** (Mode A) for now. Keep it minimal, understated, and clean — this is a work-samples page requested by a CEO, **not** a pitch deck, so no headlines, taglines, or self-promotional copy beyond the optional one-line intro. Handle both landscape and vertical videos gracefully. No autoplay; click-to-play with sound.

---

*Assets live in two folders: most clips in `portfolio_assets/`; the two HD masters (#3, #7) in `COHERE EXAMPLES HTML/drive-download-20260702T200142Z-3-001/`. Contact-sheet stills for each clip are in `portfolio_assets/_contactsheets/`.*
