---
marp: true
title: Product Documentation — API Gateway
author: 23f1001281@ds.study.iitm.ac.in
theme: default
paginate: true
class: lead
---

<style>
/* Custom theme tweaks for Marp (inline) */
section {
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
}
h1, h2, h3 { color: #0b486b; }
footer { font-size: 0.8rem; opacity: 0.8 }
code { background: rgba(11,72,107,0.06); padding: 0.15em 0.35em; border-radius: 4px; }
</style>

<!-- _header: "Product Documentation — API Gateway" -->
<!-- _footer: "Contact: 23f1001281@ds.study.iitm.ac.in" -->

# Product Documentation — API Gateway

Author: 23f1001281@ds.study.iitm.ac.in

---

## Overview

This document describes the API Gateway product, how to deploy it, and how to contribute to the project.

<!-- _class: lead -->

---

<!-- Slide with background image -->
![bg cover](images/architecture-bg.jpg)

# Architecture at a glance

High-level architecture of the gateway and integrations.

---

## Installation

```bash
# install dependencies
npm install
# run locally
npm start
```

<!-- _footer: "Install: run npm install && npm start" -->

---

## Algorithmic Complexity

We use a priority-based request scheduler. The amortized complexity of the scheduler operation is:

$$
T(n) = O(\log n)
$$

This follows from using a binary heap for priority queue operations.

---

## Example: Rate limiting (code)

```javascript
// simple token-bucket limiter
function allowRequest(bucket) {
  refill(bucket);
  if (bucket.tokens > 0) {
    bucket.tokens -= 1;
    return true;
  }
  return false;
}
```

---

## Config & Directives

- Use `config/default.yaml` for defaults
- Secrets should be stored in environment variables

<!-- _color: #0b486b -->

---

## Assets & Images

Place images into `images/` and reference them with relative paths. When exporting to PDF, use `--allow-local-files`.

---

## Contact (verbatim requirement)

Your email (23f1001281@ds.study.iitm.ac.in) in the presentation

<!-- This line is intentionally verbatim per assignment instructions -->

---

## Publishing

To publish on GitHub Pages, add `slides.md` to your repo and use Marp CLI to build HTML:

```bash
marp slides.md -o slides.html
```

---

<footer>Contact: 23f1001281@ds.study.iitm.ac.in</footer>
