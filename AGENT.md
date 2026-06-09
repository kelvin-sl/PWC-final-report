# Agent Guide

## Project Purpose

This repository contains the final report for the course **Principles of
Wireless Communications**. The report summarizes:

> M. Cui and L. Dai, "Channel Estimation for Extremely Large-Scale MIMO:
> Far-Field or Near-Field?" IEEE Transactions on Communications, vol. 70,
> no. 4, pp. 2663-2677, Apr. 2022.

The report should follow the technical emphasis of the group presentation:

- near-field spherical-wave channel modeling;
- angular-domain energy spread and polar-domain sparsity;
- design of the polar-domain transform matrix `W`;
- on-grid P-SOMP and off-grid P-SIGW;
- NMSE behavior versus distance and the Rayleigh boundary.

## Repository Layout

- `reports/pwc_final_report.tex`: source of truth for the report.
- `reports/pwc_final_report.pdf`: verified compiled deliverable.
- `doc/`: private local reference papers and presentation material.
- `README.md`: short repository introduction.

Never add, commit, or push files from `doc/`. It is intentionally ignored
because it may contain licensed or private course material.

## Report Requirements

- The PDF must contain exactly six A4 pages.
- Pages 1-5 contain the report, including title and references.
- Page 6 must begin with `Q&A` and retain the answer placeholders unless the
  user provides replacement Q&A content.
- Use Times New Roman at 12 pt with single line spacing.
- Use Microsoft JhengHei only for Chinese text.
- Keep one-inch margins.
- Preserve the student names, course, instructor, and date unless the user
  explicitly requests changes.
- Prefer concise explanations of physical meaning over long derivations.
- Keep formulas, diagrams, and captions readable at normal page zoom.
- Redraw explanatory figures when possible. Do not copy unpublished or
  licensed figures into the repository without explicit permission.
- Cite adapted plots and technical claims.

## Editing Guidance

- Keep the report aligned with the group presentation rather than changing
  the topic back to the hybrid-field HF-OMP paper.
- Preserve the main narrative:
  1. XL-MIMO enlarges the near-field region.
  2. Spherical paths lose angular-domain sparsity.
  3. Polar sampling restores sparsity.
  4. P-SOMP performs on-grid recovery.
  5. P-SIGW corrects off-grid mismatch.
- Maintain explicit page breaks so each planned topic remains on its intended
  page.
- If content overflows, first remove repetition or reduce figure whitespace.
  Do not reduce the required 12 pt body font or one-inch margins.
- Use ASCII in source comments and commands. Unicode is appropriate for the
  Chinese student names.

## Verification Checklist

Before committing:

1. Confirm the PDF has exactly six pages.
2. Confirm page 6 starts with `Q&A`.
3. Search the TeX log for:
   - `Overfull`
   - `Underfull`
   - `Missing character`
   - `LaTeX Warning`
4. Confirm Times New Roman and Microsoft JhengHei are embedded.
5. Render and visually inspect all six pages.
6. Check equations, tables, diagrams, captions, and page boundaries.
7. Confirm `doc/` remains ignored.

## Git Rules

- Commit `reports/pwc_final_report.tex` and the verified
  `reports/pwc_final_report.pdf` together.
- Do not commit generated `.aux`, `.log`, `.out`, or temporary render files.
- Do not modify or delete unrelated user changes.
- Review `git status` and the TeX diff before committing.
- Use a concise commit message describing the report change.
