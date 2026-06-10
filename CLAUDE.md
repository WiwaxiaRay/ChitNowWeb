# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-file static website for **ChitNow** — an AI agent approval system for Apple Watch. Hosted on GitHub Pages at `https://wiwaxiaray.github.io/ChitNowWeb/`.

No build step. No dependencies. Edit `index.html` and push.

## i18n

All user-visible text lives in the `i18n` JS object at the bottom of `index.html`, keyed by `en`, `zh`, `ja`. Every translatable element has a `data-i18n="key"` attribute; `setLang()` sets `innerHTML` on each. Code blocks (shell commands) are intentionally not translated.

To add a language: add a new key block to `i18n`, a `<button class="lang-btn" data-lang="xx">` in the nav, and a entry in `LANG_META` / `TITLES`.

## Deploy

Push to `main` → GitHub Pages serves `index.html` from the repo root automatically. No CI needed.
