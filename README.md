# World Bible

An AI-assisted generator for fictional worlds, with over a million combinations of premise.
It produces an encyclopedic world bible — continents, peoples, nations, cities and
characters, each written to follow from the last — which you can then edit by hand or with
continued AI assistance.

Everything runs on your own machine unless you choose otherwise.

## Download

### **[⬇ Download the latest installer](../../releases/latest)**

Windows 10/11, 64-bit. Installs for the current user — no administrator rights needed.

> **Windows will warn you the first time.** The installer is not code-signed yet, so
> SmartScreen shows a blue *"Windows protected your PC"* box. Click **More info** →
> **Run anyway**. That is what an unsigned installer looks like, not a sign of a problem.

## What you need

World Bible writes using a large language model, and you choose which one.

| | Speed | Cost | Privacy |
|---|---|---|---|
| **[Ollama](https://ollama.com) on your machine** | ~1 hour per world | Free | Nothing leaves your computer |
| **Anthropic / OpenAI / Gemini** | Minutes per world | Pay per world | Prompts go to the provider |

For the local option, install Ollama and pull a model:

```
ollama pull llama3.1:8b
```

For the hosted option, paste an API key during setup. You can change this at any time, and
mix the two — a fast hosted Generator with a local Proofreader, or the reverse.

**If generation feels slow, that is your model choice, not the app.**

## First run

The app opens with a finished sample world, **Pangrella**, already loaded — so you can read
a complete world bible, follow its cross-references and export it to a book without
generating anything first.

## What it does

- **Six tiers of detail** — World → Continent → Peoples & Nations → Cities → Characters,
  each inheriting everything established above it
- **A rolled premise** that every part of the world must obey, so no two worlds blur together
- **A chronicle** that turns one-line historical stubs into full accounts
- **Pinned people** — figures the world names but never describes are queued up for you to
  create
- **Renaming that actually works** — changes every mention across the whole world, not just
  a label
- **Exports** to HTML (self-contained, with working cross-references), Word (.docx) and
  Markdown

## Your worlds are yours

Worlds are saved as plain, readable folders in `Documents\World Bibles` — not locked inside
a database. Back one up by copying the folder; share one by zipping it.

## Documentation

**[📖 User Manual](manual.html)** — setup, world structure, exporting, speed and
troubleshooting. Also installed with the app and linked from your Start Menu.

---

Issues and feature requests: [issue tracker](../../issues).
