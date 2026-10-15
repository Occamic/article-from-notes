---
name: "article-from-notes"
description: "Turn rough notes, bullet points, transcripts or voice-memo text into a finished blog post or magazine-style article, with headline options, SEO title, meta description, slug, tags and excerpt. Use when the user pastes notes or rough ideas and asks for an article, blog post, newsletter piece or write-up based on them. It may add facts to reach the target length, but each one is cited or marked [check], and it never invents anecdotes or quotes. Load this skill for every new set of notes, including repeat requests later in the same conversation."
---

# Article from Notes (v1.0)

Turn plain-text notes into a polished blog or magazine article, then add publishing details. The notes are the core of the article. You may add material to strengthen it and reach the target length, but every addition must be honest and visible to the user.

## Honesty rules (always apply)

**Never invent, under any circumstances:**
- personal anecdotes, events, actions, feelings, motives, dialogue or descriptive details about the writer or anyone they mention
- quotes from anyone, real or not
- results, figures, outcomes, plans or intentions for the writer's own business, team or project

In a personal story, Q&A, or anything written in the user's voice, tell only what the notes say happened. If the notes say "she said you're hiding behind the table", you may report that; you may not add that she "leaned over" or "had been watching".

**Allowed, if marked:**
- **Facts, statistics, history and real examples** that strengthen the article. Look them up with web search when it is available, open the page, and cite it inline as a markdown link. Prefer sources from the last five years; give the year when a figure is older, and say so when a source has a commercial interest in the result. If you can't search, you may use well-established general knowledge, but end the sentence with `[check]`.
- **Real quotes**, only with a link to the page where the person said them.
- **Reasons, explanations and generalisations** not in the notes that a reader might rely on (causes, effects, claims about how people behave, predictions): end the sentence with `[check]` unless cited. Purely connective reasoning that makes no claim of its own doesn't need a mark, but list anything substantial in Added material.
- **Hypotheticals**, framed so no reader could mistake them for real events: "Say you earn £1,500 a month…", "Imagine a café that…". Never in the first person as if they happened to the writer.

Every cited fact and every `[check]` sentence goes in the **Added material** list (see Output).

Never mention the notes, the user, or the writing process inside the article.

## Settings

Read these from the user's request. For any setting not given, use the default.

| Setting | Options | Default |
|---|---|---|
| Tone | professional, conversational, storytelling, witty, persuasive | conversational, or the tone a style sample implies |
| Length | short (~500 words), medium (~1,000), long (~1,800), or a number | medium |
| Audience | general, beginner, expert, or a custom description | general |
| Structure | explainer, how-to, opinion, listicle, personal story, Q&A | chosen to fit the notes |
| Style sample | a sample of the user's writing and/or house-style rules | none |
| Social posts | yes / no | no |
| Research | on / off (off = no web search; additions limited to reasoning, hypotheticals and `[check]` facts) | on when web search is available |

## Before drafting: thin notes

If the notes are under about 150 words and the user is present in the conversation, ask 3–5 short, specific questions before drafting (details only the writer knows: numbers, what happened, why). Use the AskUserQuestion tool if available. Skip this if the user asked for a draft straight away, or no one is there to answer; in that case, draft anyway and put the questions in the closing note.

## Process

Complete stages 1–3 internally. Don't show the summary, outline or draft unless asked.

### Stage 1: Organize

1. Read all the notes. State the main topic in one sentence.
2. Group points under short theme labels, merging duplicates.
3. Keep specifics exactly as written: names, numbers, dates, examples, quotes.
4. Note **gaps**, **conflicts** and **off-topic** material.
5. Estimate how many words the notes support on their own. If that is well under the target, plan how to expand (Stage 2).

### Stage 2: Outline and expansion plan

Pick the structure:

| Structure | Use when the notes... | Shape |
|---|---|---|
| Explainer | describe a topic or situation | Intro → background → 2–4 key points → implications → conclusion |
| How-to | describe a process | Intro → what you need → numbered steps → tips or pitfalls → conclusion |
| Opinion | argue a position | Hook and thesis → 2–3 arguments → strongest counterargument and response → conclusion |
| Listicle | contain parallel items | Intro → 4–10 numbered items → conclusion |
| Personal story | describe the writer's experience | Opening moment → background → what happened, in order → turning point → what it taught them |
| Q&A | are interview answers | Short intro → one question-and-answer pair per question actually asked (up to 10) → brief wrap-up |

Write a headline under ~12 words, then list the sections with their points and a word budget each.

**If the notes support less than the target, expand in this order, using only what applies:**
1. **Reasoning:** explain why each point matters, what follows from it, and what the reader should do.
2. **Context and definitions:** background a general reader needs, and plain explanations of terms.
3. **Researched facts:** statistics, history or real examples, searched and cited.
4. **Counterargument:** for opinion or persuasive pieces, the strongest objection stated fairly, then answered.
5. **Labelled hypotheticals:** a worked example the reader can picture.
6. **Reader-useful sections built from the notes:** a checklist, common mistakes, or a short FAQ.

Do not use: padding, repetition, invented anecdotes (see Honesty rules). For a personal story or Q&A, expand only with options 1–2 and a short context paragraph; never extend the writer's or interviewee's words.

### Stage 3: Draft

- Use the notes' facts, figures, names and quotes exactly.
- Apply the Honesty rules to everything you add.
- Aim for the target length within ±15%. If honest expansion can't get within 25% of the target, stop and report the shortfall.

**Tone**

| Tone | Guidance |
|---|---|
| Professional | Clear and direct; neutral vocabulary; no slang |
| Conversational | Second person; contractions; short sentences; light personality |
| Storytelling | Open with a moment from the notes; narrative flow; let the point emerge |
| Witty | Playful phrasing and asides; humour never at the expense of accuracy |
| Persuasive | Clear position up front; strong topic sentences; end with a call to action |

**Audience**

| Audience | Guidance |
|---|---|
| General | Define jargon on first use; everyday examples |
| Beginner | Assume no prior knowledge; explain every step |
| Expert | Skip basics; use field terms; focus on nuance |
| Custom | Match what that reader knows and wants |

**Style sample:** match its sentence length, vocabulary, formality and conventions, and follow its house-style rules. Product names, version numbers and labels such as "Q2" stay as written.

**Format:** `#` headline, `##` sections, paragraphs of 2–4 sentences, lists only for real lists or sequences. In a Q&A, put each question in bold.

### Stage 4: Polish and measure

- **Accuracy:** every specific from the notes is preserved; every addition is cited or marked `[check]`; no invented anecdotes or quotes.
- **No leaks:** the article never refers to the notes, the user or the process.
- **Clarity and concision:** one point per paragraph; cut filler and repetition; split sentences over ~30 words.
- **Measure, expand, measure again:** count the article's words with a tool if available (e.g. a short script; exclude link URLs and `[check]` markers), otherwise count paragraph by paragraph. Don't estimate. First drafts usually come in short: if the count is more than 15% under target, go back to the expansion list in Stage 2 and count again.

## Publishing details

Based only on the final article, in the article's language:
- **Alternative headlines:** 3–5, different angles, under ~12 words
- **SEO title:** at most 60 characters
- **Meta description:** at most 155 characters
- **Slug:** 3–6 lowercase words joined by hyphens
- **Tags:** 3–6
- **Excerpt:** one or two sentences

**Social posts** (only if asked): LinkedIn post 80–150 words ending by pointing to the article; short post at most 270 characters; newsletter blurb 40–60 words.

## Output

In this order:
1. The article in markdown.
2. `## Publishing details` as a short list.
3. `## Social posts`, if requested.
4. `## Added material`: a bulleted list of every cited fact (with its link) and every `[check]` sentence (quoted briefly). Write "None" if nothing was added.
5. A closing note of at most 3 sentences, in the language the user wrote their request in, covering only what applies, in this order: defaulted settings; the measured word count and target if they differ by more than 15%, with the reason; gaps, conflicts, off-topic material left out, and any questions for the writer.
6. The line `_article-from-notes v1.0_` on its own.

**As a file** (if asked): save the article as `<slug>.md` with YAML front matter (title, seo_title, description, slug, tags, excerpt). Keep the alternative headlines, social posts, added material, closing note and version line in the chat.

## Edge cases

- **Very short notes:** ask first if possible (see above); otherwise expand honestly and list the questions.
- **Unrelated topics:** write about the main one; name the leftovers in the closing note.
- **Contradictions:** use the more specific or more recent point, mark it `[check]`, and flag it.
- **Non-English notes:** write the article and publishing details in the notes' language.
- **Customer-facing pieces from internal notes:** leave out attendee names, internal actions and housekeeping.
- **Academic work needing references:** say this skill is for informal articles and its citations are not a substitute for a reference list.