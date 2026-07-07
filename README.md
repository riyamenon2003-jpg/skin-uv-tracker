# SkinScope

A public web tool for UV safety and skin self-checks — built as a v2 of an earlier concept (AI image analysis + wearable UV sensor data) reworked into something anyone can use today, no hardware required.

**Live app:** https://riyamenon2003-jpg.github.io/skin-uv-tracker/

## What it does

- **Today dashboard** — a single at-a-glance view of the day: current UV reading, minutes logged outside vs. your safe-exposure budget, your skin type, and how long it's been since your last mole journal entry
- **UV Tracker** — live UV index by city, a same-day UV curve, and an estimated safe-exposure time personalized to your skin type
- **Fitzpatrick skin type quiz** — a real dermatology classification used to personalize the exposure estimate, with a direct link back to see your resulting safe-minutes estimate
- **Sun Log** — log time spent outside manually, or import "Time in Daylight" data from an Apple Health export, tracked against your daily safe-exposure budget
- **Compare Guide** — illustrated (not photographic) ABCDE reference pairs so you can learn what each warning sign looks like, plus a place to view your own photo alongside them for self-comparison, and a link to the American Academy of Dermatology's dermatologist-reviewed photo galleries for real examples
- **Mole Journal** — photo + note log for tracking a spot over time, with a reminder if it's been a while since your last entry

## Why this design

Skin cancer detection tools built on unverified image classification are a common (and risky) approach — a small model can't reliably diagnose a mole from a phone photo, and a database "closest match" search carries the same risk even without saying the word "diagnosis." SkinScope is intentionally scoped around what's safe and useful: real-time UV data, a validated skin-type framework, an illustrated (not photographic) self-check guide, and a change-tracking journal that always routes anything concerning to a dermatologist. The goal is showing where AI/software should assist clinical judgment, not replace it.

## Tech

Single-file HTML/CSS/JS. UV and geocoding data from the free [Open-Meteo API](https://open-meteo.com) (no key required). Data (mole journal entries, skin type, sun log) is stored locally in the browser via `localStorage`, so it stays on-device and persists across visits without a backend. Deployed via GitHub Pages.

## Background

This builds on an earlier SkinScope concept combining AI-based image analysis with wearable UV sensor data. This version trades the hardware dependency for something anyone can open in a browser today.
