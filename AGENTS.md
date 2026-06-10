# AGENTS.md

This file provides guidance to Codex (codex.com) when working with code in this repository.

## What this is

A single-file static website for **ChitNow** — an AI agent approval system for Apple Watch. Hosted on GitHub Pages at `https://wiwaxiaray.github.io/ChitNowWeb/`.

No build step. No dependencies. Edit `index.html` and push.

## Editing rules

- All user-visible text lives in the `i18n` JS object near the bottom of `index.html`, keyed by `en`, `zh`, `ja`.
- Every translatable element has a `data-i18n="key"` attribute; `setLang()` sets `innerHTML` on each.
- Shell commands in `.cmd-block` elements are intentionally not translated — do not add `data-i18n` to them.
- To add a language: add a new key block to `i18n`, a `<button class="lang-btn" data-lang="xx">` in the nav, and an entry in the `LANG_META` / `TITLES` objects at the bottom.

## Deploy

Push to `main` → GitHub Pages serves `index.html` from the repo root automatically. No CI or build command needed.

## Style

The page uses a terminal / monospace aesthetic (`SF Mono` font stack, scanline overlay, pixel mascots rendered via inline SVG). Preserve this when making changes. Color variables are defined in `:root` at the top of the `<style>` block.
