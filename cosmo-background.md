# About Cosmo

**[🌌 Chat with Cosmo →](https://[cosmo-the-chatbot.web.app/cosmo.html])**

---

## Overview

In a world of flawless AI and polished automation, Cosmo represents a different approach: one that values authenticity over perfection, and human connection over technical sophistication. Cosmo is a JavaScript-based conversational interface built to explore two ideas: first, that technology doesn't need to know everything to be useful; and second, that vulnerability—even in code—can be a form of strength.

Cosmo is a guided reflection of my journey, built conversation by conversation. He is designed to answer questions about my journey, projects, skills, and experience, with a personality that acknowledges its own limitations.

**Author:** Niha Salman

---

## Why Cosmo Exists

While navigating the "no degree, no experience" paradox of the tech industry, I noticed an implicit pressure to present as omniscient—to mask uncertainty, hide gaps, and perform expertise.

Cosmo is a response to that pressure. He is, in many ways, an argument: **you don't need to be perfect to build something with purpose.**

He is also a testament to self-teaching. Every response he gives was manually written, edited, and structured—a curated database of over 100 Q&As that reflect not just what I know, but how I think.

---

## What Makes Cosmo Different

- **Honest by design:** He will say "I don't know yet" — and mean it.
- **Database-driven:** His knowledge lives in Firebase Firestore, allowing updates without code changes.
- **Manually curated:** His knowledge comes entirely from what I have taught him, ensuring accuracy and alignment with my actual experience.
- **Human-paced:** Responses feel conversational, not instantaneous—complete with pauses, reflections, and occasional wit.
- **Focused in scope:** He answers questions about me and my work, not the universe.

Cosmo isn't competing with any AI Model. He's here to offer a more personal, transparent, and deliberately limited kind of interaction.

---

## What You Can Ask

Try questions like:

- "Who is Niha?"
- "What does she do?"
- "What specific AI skills does Niha have?"
- "What is she working on now?"
- "Why did Niha build Cosmo?"

Cosmo responds once per message, with no memory between exchanges. Each interaction is self-contained—a single thought, clearly framed.

---

## For Recruiters & Collaborators

Yes, Cosmo knows I'm actively exploring roles at the intersection of AI, ethics, and human behavior. He can speak to:

- My technical skills and project experience
- My approach to problem-solving and learning
- How to contact me or review my work
- The kinds of challenges I'm looking for next

If he doesn't have an answer, he'll admit it.

---

## What Cosmo Is Not

- A code or content generator
- A replacement for human conversation
- An always-improving AI model
- A general-purpose assistant

He is, instead, a conversational portfolio piece—a way to engage with my story through dialogue rather than a static page.

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| Frontend | HTML5, CSS3, JavaScript (ES6+) |
| Database | Google Firebase Firestore |
| Logic | Custom-built scoring algorithm (Non-LLM based for 100% factual accuracy) |

---

## Features

- **Hybrid Search Engine:** Combines exact match, variation matching, and keyword relevance scoring
- **Local Intelligence:** Fetches knowledge documents and performs real-time ranking in the browser for instant results
- **Smart Caching:** Implements a 5-minute memory system to reduce database hits and improve performance
- **Heuristic Fallbacks:** Includes emergency response logic for critical questions (Contact, Identity, Experience) if connectivity is limited
- **Security Hardened:** Integrated with Firestore Security Rules and request-limiting to prevent data scraping

---

## Security Configuration

This project uses a **"Tight-Limit" security model**:

- **Read Access:** Restricted to queries with a `.limit(200)` to prevent bulk data extraction
- **Write Access:** Strictly disabled (`allow write: if false`) to prevent unauthorized database modifications
- **App Integrity:** Compatible with Firebase App Check

---

## How to Update Knowledge

Knowledge is managed via the **Firestore Console** in the `cosmo_knowledge` collection. Each document supports:

| Field | Description |
|-------|-------------|
| `question` | The primary trigger |
| `answer` | The verified response |
| `variations` | An array of alternative ways to ask the same thing |
| `priority` | Numeric weight to boost specific answers |

---

## A Final Note

Cosmo is built entirely in JavaScript, with a handcrafted knowledge base. Nothing he says is generated live by an external AI. Every response was written by me, for him.

This makes him less scalable, but more personal—a small artifact of what it means to build thoughtfully, learn publicly, and present yourself not as finished, but as in progress.

---

*Last Updated: 2026*
