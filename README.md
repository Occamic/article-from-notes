# Article from Notes

An AI agent skill that turns rough notes into a finished blog post or magazine-style article, ready to publish.

Paste in bullet points, a meeting write-up, a transcript or voice-memo text. You get back:

- **the article**, organised and written to your chosen tone, length and audience
- **publishing details**: alternative headlines, SEO title, meta description, URL slug, tags and an excerpt
- **an "Added material" list** of everything that wasn't in your notes, so you can check it before publishing
- optional **social posts**: a LinkedIn post, a short post for X or Bluesky, and a newsletter blurb

Works with Claude (app and Claude Code) and other agents that support `SKILL.md` skills, such as Codex and Cursor.

## Honest by design

Thin notes usually produce thin articles, and AI tools tend to pad them with made-up detail. This skill doesn't:

- **It never invents** anecdotes, quotes, or results for you or your business.
- **It may add facts** to reach the target length, but each one is either cited with a link (when web search is available) or marked `[check]` for you to verify.
- **Every addition is listed** under "Added material" at the end of the reply.
- **If the notes are very short,** it asks you a few questions first instead of guessing.

## Example

[Notes in](examples/four-day-week-notes.txt) (154 words of rough bullets about a team's four-day-week trial), with the request *"Write a short, conversational article for small-business owners"*.

[Article out](examples/four-day-week-output.md): a 483-word article with headings, two cited facts from a UK pilot study, four sentences marked `[check]`, and full publishing details.

## Install

**Claude app (web, desktop, mobile)**
1. Download `article-from-notes.zip` from the [latest release](../../releases/latest).
2. In Claude, open the Skills section of your settings and choose **Upload skill**. Custom skills need a paid plan, with code execution turned on.

**Claude Code (as a plugin)**
```
claude plugin marketplace add YOUR-GITHUB-USERNAME/article-from-notes
claude plugin install article-from-notes@article-from-notes
```

**Claude Code (manual) and other agents**
Copy the `skills/article-from-notes` folder into your agent's skills directory, for example `~/.claude/skills/` for Claude Code.

## Use

Start your message with `/article-from-notes`, or just ask for an article and paste your notes:

> /article-from-notes Write a 1,000-word professional article for marketing managers from these notes: …

Anything you don't specify uses a sensible default:

| Setting | Options | Default |
|---|---|---|
| Tone | professional, conversational, storytelling, witty, persuasive | conversational |
| Length | short (~500 words), medium (~1,000), long (~1,800), or a number | medium |
| Audience | general, beginner, expert, or describe your reader | general |
| Structure | explainer, how-to, opinion, listicle, personal story, Q&A | best fit for the notes |
| Style sample | paste a sample of your writing or house-style rules | none |
| Social posts | yes / no | no |
| Research | on / off | on when web search is available |

Ask for a file and it saves the article as `<slug>.md` with YAML front matter (title, SEO title, description, slug, tags, excerpt), which Hugo, Jekyll, Ghost and most markdown blog tools can read.

## Tips

- **Use one article per chat.** In a long chat the AI may reuse earlier instructions instead of loading the skill again.
- **Check for the version line.** Every reply from this skill ends with *article-from-notes v1.0*. If it's missing, start a new chat or begin your message with `/article-from-notes`.
- **Read the Added material list before publishing,** and verify anything marked `[check]`.

## Limitations

- It's built for informal articles such as blog posts, newsletters and magazine pieces. Its citations are not a substitute for a reference list in academic work.
- Research needs web search to be available in your agent. Without it, any added facts are marked `[check]` instead of cited.
- As with any AI writing, read the result before you publish it.

## Licence

MIT. See [LICENSE](LICENSE).
