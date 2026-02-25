# EthosLink - AI-Powered Business Solutions

<p align="center">
  <img src="assets/ethoslink-logo.svg" alt="EthosLink - AI-powered business solutions" width="250" />
</p>

<p align="center">
  <a href="https://www.ethos-link.com/">
    <strong>Ethos Link</strong>
  </a>
</p>

<h1 align="center">Software that fits how you actually work</h1>
<p align="center"><em>Human service, thoughtful AI.</em></p>

<p align="center">
  We build software for hospitality and service teams that need useful answers fast, not heavy setup.
  Get the signal, take action, and get back to work.
</p>

<p align="center">
  <a href="https://www.ethos-link.com/about/">About</a> ·
  <a href="https://www.ethos-link.com/contact/">Contact</a> ·
  <a href="https://www.reviato.com/">Our product: Reviato</a>
</p>

---

Ethos Link builds pragmatic software that helps small and medium businesses adopt “high-tech” workflows without high-tech overhead.

**Reviato** is our flagship product: a review intelligence platform for hospitality and service operators. It unifies reviews + feedback across platforms, turns them into plain-language insights, and helps teams act consistently.

- Company: <https://www.ethos-link.com>
- Product: <https://www.reviato.com>

---

## Mission

Ethos Link exists to close the gap between modern technology and SMBs by shipping solutions that optimize workflows and increase revenue.

We build in public when it’s useful to other developers, founders, and operators—especially around infrastructure, deployment, and the “boring” reliability work required to keep products running.

---

## Reviato (a product of Ethos Link)

Reviato helps teams stay on top of customer sentiment without spending their week inside review platforms.

What it does (high level):

- Aggregates reviews from platforms like Google, TripAdvisor, and OTAs
- Runs sentiment + aspect analysis to surface patterns (what’s working, what’s slipping)
- Produces digestible summaries for operators (daily/weekly)
- Supports multi-location teams and role-aware workflows

If you’re building in hospitality, retail, or any feedback-heavy business: the problem isn’t “more data”, it’s getting to the next best action quickly.

---

## A real work example (extracted)

A common workflow we ship in Reviato is the **“morning snapshot”**:

- Ingest new reviews and in-house appraisals overnight
- Classify sentiment and extract key aspects (service, cleanliness, value, location)
- Highlight anomalies (rating drops, recurring complaints, sudden spikes)
- Generate a short summary email with suggested actions per location

This sounds simple, but it’s a real production pipeline with a few non-negotiables:

- Idempotent ingestion across multiple providers
- Background jobs + retries (provider APIs fail; your customers shouldn’t notice)
- A database that can sustain bursts of writes + reads (and still be recoverable)
- Clear operational tooling (backups, restores, logging, runbooks)

That’s the kind of engineering Ethos Link focuses on: systems that don’t add cognitive load to already-busy teams.

---

## 🏗️ This Repository

This repository contains the source code for the EthosLink company website, built with:

- **Jekyll** - Static site generator
- **Tailwind CSS** - Utility-first CSS framework
- **GitHub Pages** - Hosting and deployment
- **Custom components** - Responsive design and modern UI

### Local Development

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

---

*© 2026 EthosLink, Inc. All rights reserved.*
