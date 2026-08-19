---
fonte_url: https://ericmjl.github.io/blog/2026/3/6/mastering-personal-knowledge-management-with-obsidian-and-ai/
autor: Eric J. Ma
capturado: 2026-08-18
---

# Mastering Personal Knowledge Management with Obsidian and AI

Folks have asked me how I do personal knowledge management (PKM) at work. The question becomes more pressing when they learn how many projects and people I need to interact with on a weekly basis. At the time of writing, I manage twelve people across two teams, each handling 2-4 projects of their own. That's a lot of context to keep straight.

I decided to document what I'm doing for PKM. Hopefully it serves as inspiration for you.

I've written before about why I chose Obsidian; this post shows how that decision evolved with AI integration over five years.

## The plain text decision

In 2022, I decided to make personal knowledge management a priority at work. I faced a choice: Confluence, OneNote, or a new kid on the block, Obsidian. I chose plain text and graphs. I chose Obsidian. I chose not to lock my data inside a vendor system. I chose freedom and sovereignty for my information.

That decision was prescient in ways I couldn't have predicted. Most of us back then wouldn't have guessed that plain text would be exactly the right format for 2025 and 2026 era knowledge management. The visionaries saw it coming; I just got lucky because I loved the graph view in Obsidian and thought of it as a really cool tool. But that choice has paid off tremendously.

"Text files are as primitive as it gets: no proprietary formats, no vendor lock-in, just files that can be read on any system." When AI coding agents arrived, the vault was already in a format they could process natively. No migration needed. No conversion layer. No API integration. The simplicity chosen became an unlock never planned for.

## The core system

The Obsidian vault is built around distinct note types. Monthly collections of daily bullet journals capture day-to-day activities, one note per month with a running log of meetings and work. Meeting notes follow a structured template. People notes are dossiers for everyone worked with regularly. Project notes act as control towers, linking out to meetings, people, and status updates. A miscellaneous collection handles everything else. The structure was inspired in part by Thiago Forte's numbered folder system, though it has been simplified over time.

"The most important thing isn't my specific implementation. It's that I have a system at all, and it's documented in an `AGENTS.md` file so my coding agents understand it too."

## Ingesting information

The lifecycle of the workflow starts with ingestion. Meeting notes arrive as transcripts or AI-generated summaries. In the past, structuring these was tedious work. Now they are pasted into OpenCode and the meeting notes skill handles the rest.

The skill knows the template desired. It handles various input formats: AI-generated summaries, transcripts with good speaker assignments, and transcripts with poor speaker assignments. Quality flags are used when known to be bad. The skill extracts key information and formats everything consistently. For one-on-ones, it ensures notes are attached to both the meeting log and the person's individual page, so the full history of conversations can be tracked.

Beyond meetings, PowerPoints, Word docs, PDFs, and Excel spreadsheets are ingested into the vault as contextual information. "The key insight is getting everything into plain text format." For Word documents, a Python script converts them to plain text using `python-docx`, which is then printed to the terminal or dumped to disk at `/tmp`, both readable by a coding agent. Even lightly misformatted plain text contains enough information density for a coding agent to read and summarize.

For PowerPoints, dual parsing paths are used. One path extracts the XML structure directly using `python-pptx`. The second path converts each slide to an image using `libreoffice` and `PIL`, captions it with a vision-language model via APIs, and strings the captions together into a coherent narrative. Combined, an estimated 90-95% accurate textual representation can be obtained. PDFs follow a similar pattern: text extraction for normal PDFs, image captioning for scanned documents.

Excel spreadsheets are read directly by the coding agent using `openpyxl`, not `pandas`. "The key difference matters: `pandas` assumes an established table structure, but real-world spreadsheets are messy." With `openpyxl`, the agent can read the granular cellular structure across each sheet, identifying merged cells, free text scattered in random locations, and arbitrary layouts. This structural mapping follows a progressive reveal principle: the agent first identifies the spreadsheet's architecture without necessarily reading every cell's contents, then zooms into relevant sections. This approach handles the chaos of actual spreadsheets far better than forcing everything into a tabular assumption. It's powerful when needing to understand financial data without being a finance person.

## Managing and maintaining

With information in the vault, the next phase is keeping it current. With twelve people across two teams, there are a lot of details that don't get picked up or retained in working memory. That's why external memory matters. Without it, things would fall through the cracks.

When hitting a context block (when looking up a project or person and realizing something's missing), a "sweep" is triggered. Instructions to the coding agent are to update people notes and/or project notes based on source material present in the vault. "People and project notes are always derivative from sources, so any updates must include quotations from those source notes." The user stays in the loop for verification. Hallucinations are rare, maybe once every four or five sweeps, and usually trace back to inaccurate transcripts rather than agent errors.

This is incredibly helpful for how people are interacted with. The assumption is that forgetfulness will occur. External memory will be approximately correct, and there is a process for keeping it refined over time. So reliance on the vault can be increased instead of second-guessing based on incomplete memory. It tempers how thinking about interacting with someone works, not by changing the mind about them, but by giving confidence that nothing important is being missed.

There are ethical boundaries. Personal details are not captured if people aren't comfortable with that. The dossiers are professional, not invasive.

Periodically, retrieval practice is done. This is how information sticks; the book "Make It Stick" explains this more. Review looks like this: people notes and project notes are taken and reviewed for what's missing. Is there a piece of knowledge remembered that isn't captured? If yes, the blanks are filled in. Claims are also checked for substantiation with links and quotes. This fact-checking pass keeps the vault trustworthy and protects from remembering something erroneous. A spell-checker list handles transcription errors, and `AGENTS.md` links to `HEARTBEAT.md` to sanitize the vault of inaccurate information.

## Producing and sharing

The final phase is producing outputs for others. What gets published is curated rather than exporting everything. The agent creates a publishable version based on guidance provided. Hard rules for curation haven't been settled on yet. The preference is to review and decide at publish time rather than tag things as publishable during capture. That workflow feels right.

For Confluence, a Python script publishes markdown directly, with YAML front matter defining the space and parent page. For GitHub users, notes can become Gists via the GitHub CLI. With the appropriate skills, Markdown files transform into HTML presentations, and with web technologies, those presentations become interactive. For Jira, a colleague created a skill that writes Jira tickets. The firm belief is that humans shouldn't be filling forms out; AI should be filling forms for us.

PowerPoint decks can be generated via Python scripts. Word documents come from markdown via Pandoc. The scripts run with uv, and LibreOffice handles conversions.

Each script maintains its own environment using PEP 723 inline script metadata. This means dependencies are declared at the top of each script in a special comment block:

```
# /// script
# dependencies = ["python-docx", "python-pptx", "pandas"]
# ///
```

When `uv run script.py` is executed, uv automatically creates an isolated environment with just those dependencies, executes the script, and cleans up. No virtual environments to manage. No `requirements.txt` files scattered everywhere. No "works on my machine" problems.

## The role of agent skills

"Agent skills effectively encode procedural knowledge into executable markdown." Over time, it compounds; on fewer and fewer occasions is instruction repetition needed, which is incredibly liberating. The model infers which skill to use most of the time. When it doesn't, correction is made explicitly and the coding agent is asked to update the skill file for the future as well.

Designing a skill means thinking about the desired output and the tools needed to get there. Edge cases are discovered in the wild and updated immediately. The earlier errors are caught, the better.

## What's still friction

One pain point remains. Ingestion of Office files by pasting a URL is desired, but a copy still needs to be downloaded first, then fed to the agent skill. Programmatic access to cloud documents would eliminate this step. From the user side, nothing else would change. The URL would just be pasted and things would proceed.

But even with this friction, the system pays for itself. "Knowledge management overhead dropped from thirty to forty percent of my time down to less than ten percent." Errors are fixed as they are encountered rather than scheduling dedicated maintenance. That recovered bandwidth goes toward better thinking and context gathering.

## Getting started

What stops people from building systems like this? It is believed to be two things: imagination and technical skill. Imagination is needed to envision converting diverse file formats into plain text. Technical skill is needed to know that it's possible.

The two feed each other. This was experienced with web technologies. Before becoming familiar with building stuff on the web, there was wonder about what was even possible. Once things were actually built, knowledge came. Technical skill feeds imagination, and imagination drives learning more technical skills.

For those starting without technical skills, AI can be used to learn programming. A language with a supportive human community should be found to verify what is learned. AI hallucinates, and other people are needed around to help apply judgment and skill to AI outputs. Critical thinking skills and the initiative to act on what agents produce are also needed.

## Skills you can use today

If you want to experiment with agent skills, here are some published:

- html-presentations - Turn markdown into gorgeous HTML slides
- gh-daily-timeline - See your GitHub activity for any given day
- gh-activity-summary - Generate a plain-language summary of your GitHub work over any time period
- publish-to-google-docs - Push markdown notes to Google Docs

## The bigger picture

With such a system in place, repetitive, monotonous, and manual work can be offloaded to computers and AI. With a personal knowledge system, a broader scope of responsibilities can be carried and new challenges can be grown into for two reasons: memory can be externalized more easily, and information can be formatted in ways that fit our brains.

The ask is not for people to do more at the same time. The ask is for them to expand their dynamic range over time so they're not stuck doing the same old boring thing over and over. "That repetitive monotonous stuff should have been given away to AI and computers a long time ago."

This is useful for your career. It keeps things interesting. Every day that an incremental but permanent improvement is made compounds over time.

The vignettes shared are not a prescription. Rather, they are an invitation. Plain text plus coding agents is a powerful combination. Your system will look different, and that's part of the point. Experiment and explore, and find what works for you.
