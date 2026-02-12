# ADR 001: Strict Local-First Architecture

**Date:** 2026-02-12
**Status:** Accepted

## Context
We are building a privacy-centric application. Modern software often defaults to cloud syncing, telemetry, and external SaaS dependencies, which violates user trust, data sovereignty, and breaks offline functionality.

## Decision
We will adopt a strict local-first, offline-only architecture. All databases, files, and processing (including AI/ML) must run natively on the user's hardware.

## Consequences
- **Positive:** Maximum privacy, zero latency, works offline, no recurring cloud costs.
- **Negative:** Harder to sync across devices, limited by the user's hardware capabilities.
- **Rule:** AI Agents are explicitly banned from integrating cloud SDKs (e.g., Firebase, Supabase Cloud, OpenAI API, Vercel Analytics) without explicit human override.
