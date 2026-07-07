# SkinScope

A public web tool for UV safety and skin self-checks — built as a v2 of an earlier concept (AI image analysis + wearable UV sensor data) reworked into something anyone can use today, no hardware required.

**Live app:** https://riyamenon2003-jpg.github.io/skinscope/

## What it does

- **UV Tracker** — live UV index by city, with a same-day UV curve and an estimated safe-exposure time based on skin type
- **Fitzpatrick skin type quiz** — a real dermatology classification, used to personalize the exposure estimate
- **Mole journal** — photo + note log built around the ABCDE self-check rule (Asymmetry, Border, Color, Diameter, Evolving), designed to help someone notice change over time, not diagnose

## Why this design

Skin cancer detection tools built on unverified image classification are a common (and risky) approach — a small model can't reliably diagnose a mole from a phone photo. SkinScope is intentionally scoped around what's safe and useful: real-time UV data, a validated skin-type framework, and a change-tracking journal that always routes anything concerning to a dermatologist. The goal is showing where AI/software should assist clinical judgment, not replace it.

## Tech

Single-file HTML/CSS/JS. UV and geocoding data from the free [Open-Meteo API](https://open-meteo.com) (no key required). Deployed via GitHub Pages.

## Background

This builds on an earlier SkinScope concept combining AI-based image analysis with wearable UV sensor data. This version trades the hardware dependency for something anyone can open in a browser today..
