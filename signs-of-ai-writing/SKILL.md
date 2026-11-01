---
name: signs-of-ai-writing
description: Detect and avoid the telltale patterns of AI-generated (LLM, chatbot, ChatGPT-style) writing, based on Wikipedia's "Signs of AI writing" field guide by WikiProject AI Cleanup. Use this skill whenever the user asks whether text was written by AI, wants a draft checked for "AI tells", "slop", puffery or generic chatbot prose, is reviewing Wikipedia edits, articles, essays, submissions or comments for undisclosed AI use, or wants writing revised so it reads as specific and human. Also consult it before writing or editing encyclopedic, journalistic, academic or other formal prose, where inflated significance, vague attributions, invented sources or chatbot formatting would hurt the result.
license: CC-BY-SA-4.0. Adapted from Wikipedia:Signs of AI writing; see "Credits and license" at the end of this file.
metadata:
  source: https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing
  source-snapshot: "2026-10"
---

# Signs of AI writing

A field guide to the habits of chatbot-generated prose, condensed and reorganized from Wikipedia's "Signs of AI writing" advice page, which WikiProject AI Cleanup editors built from thousands of real AI-generated edits. It has two uses.

1. Reviewing: judge whether a text shows signs of LLM generation, and find the deeper problems those signs usually point to.
2. Writing and revising: produce prose that doesn't lean on these habits, by fixing what the habits cover for instead of swapping words.

The examples in this file are invented for illustration. The patterns and word lists come from the Wikipedia page.

## Read this first

The catalog describes; it does not prescribe. Every pattern here also appears in human writing, because the models learned it from human writing: press releases, travel brochures, school essays, fan wikis, blogs. Treat each sign as a reason to look closer, never as proof.

- One sign means little. A cluster of signs from different categories means more. A single "crucial" is noise; a short draft with a dozen AI-vocabulary words, three trailing "-ing" interpretations and a "Challenges" section is a pattern.
- Automated detectors (GPTZero, Pangram and similar) beat chance but have real error rates, and they break under paraphrasing, markup changes and models they weren't trained on. Never present a detector score as a verdict.
- People are poor detectors too. Studies cited by the guide put typical readers near chance. In one 2025 study, people who use LLMs heavily for their own writing caught about 90% of AI texts while flagging about 3% of human texts. Keep your confidence modest.
- Text published before ChatGPT's public launch on 30 November 2022 is very unlikely to be LLM output, however "AI-ish" it reads.
- The surface signs matter less than what sits underneath: claims no source supports, sources that don't exist or don't say what is attributed to them, and the writer's own interpretation presented as fact. Scrubbing the signs without fixing those problems only makes the problems harder to find.
- Accusations have costs. False ones drive away newcomers and poison discussions. Describe what the text does, not what the writer is.

### Most common signs right now

As of October 2026, the guide lists these as the most frequent signs in newly AI-generated Wikipedia text, apart from the unambiguous artifacts: Markdown where it doesn't belong, AI-written edit summaries, hedging disclaimers about what sources are available, vague "associated with" / "in connection with" phrasing, and canned emphasis on media coverage and source attribution. All are covered below.

## Why AI prose looks the way it does

An LLM predicts likely continuations, so its output drifts toward whatever is statistically typical across many cases. Tuning for broad approval then pushes it toward agreeable, positive prose. Rare, specific facts get replaced with common, generic praise: "designed the first automatic railway coupler" becomes "a visionary titan of industry". The guide's image is a portrait fading from a sharp photograph into a blurry sketch while someone insists ever more loudly that the sitter is important. The subject ends up less specific and more exaggerated at the same time.

Most of the signs below are versions of that one drift. It gives you the most useful single test: could this sentence be pasted, unchanged, into an article about a different subject? If yes, it is probably filler.

## Catalog of signs

### Content

#### Inflated significance, legacy and broader trends

Ordinary details get tied to a bigger story. A founding date "marks a pivotal moment"; a new road "solidifies its role as a regional hub". This happens even for mundane material like etymology or population figures, sometimes after a hedge ("Though it saw limited use, it reflects..."). Writing about species over-stresses links to the wider ecosystem and dwells on conservation status even when nothing is known. Subjects get placed amid unnamed "debates" or "public discussions". Since mid-2026, models also editorialize about why "this distinction matters".

Words to watch: stands/serves as, is a testament/reminder, plays a vital/significant/crucial/pivotal/key role, pivotal moment, underscores/highlights its importance, reflects broader, symbolizing its ongoing/enduring/lasting, contributing to the, setting the stage for, marking/shaping the, represents/marks a shift, key turning point, evolving landscape, focal point, indelible mark, deeply rooted, the distinction matters because.

> AI-flavored: Opened in 1952, the Hollis Street Library stands as a testament to the town's enduring commitment to learning, marking a pivotal moment in the region's cultural landscape.
>
> Specific: The Hollis Street Library opened in 1952 with about 4,000 books donated by residents.

Fix: state the fact. Keep a claim of significance only if a source makes it, and attribute it to that source.

#### Canned emphasis on notability, coverage and attribution

Instead of saying what sources report, the text talks about the sources: which outlets "featured" or "profiled" the subject, what kind of outlets they are (trade press, regional media), whether coverage is "independent". Often the list of outlets comes with nothing about what they said. Asked to write for Wikipedia, models echo guideline vocabulary ("significant independent coverage") inside the article, as if arguing for notability in the text itself. People and companies "maintain an active social media presence". Trivial or uncontroversial facts get body-text attribution ("According to company filings, ...") where a footnote would do. Models also pin their own analysis on a named source. This is more common in tools released from 2025 on.

Words to watch: independent coverage, local/regional/national media outlets, music/business/tech outlets, trade publications, cited/featured/profiled in, written by a leading expert, active social media presence, was identified by.

Fix: replace the list of outlets with what one or two of them actually reported. Check that each attributed claim appears in the cited source.

#### Superficial analysis

A fact followed by a participle clause that interprets it: "..., highlighting the region's growing importance." The strongest form has an inanimate subject performing a mental act. A person can highlight or emphasize something; a bridge, a date or a statistic cannot. The "highlighting" is a claim by an invisible narrator about what something means. Search-enabled chatbots attach these claims to named sources whether or not the source says anything similar.

Words to watch: highlighting, underscoring, emphasizing, reflecting, symbolizing, showcasing, ensuring, contributing to, fostering, cultivating, encompassing, enhancing, valuable insights, aligns with, resonates with.

> AI-flavored: The bridge opened in 1931, underscoring the town's emergence as a vital trade corridor.
>
> Specific: The bridge opened in 1931 and cut the trip to Ashford from two hours to twenty minutes.

Fix: delete the trailing clause, or replace it with a concrete consequence that a source supports.

#### Promotional, brochure-like tone

Even when asked for neutral prose, models drift into ad copy or travel-guide voice, especially for places, anything that could count as "cultural heritage", companies and products. A rewrite that claims to "remove promotional tone" sometimes adds it. GPT-4-era output was openly glowing; newer models are subtler and avoid flat superlatives like "the best", but the same stock phrases recur whatever the topic.

Words to watch: boasts, vibrant, rich, profound, nestled, in the heart of, natural beauty, breathtaking, groundbreaking, renowned, showcasing, exemplifies, commitment to, diverse array, continues to captivate, featuring.

Fix: cut adjectives that judge and keep ones that measure. For "renowned", ask: renowned by whom, for what?

#### Vague connection or association

Rather than stating a relationship, the text says two things are "associated with" or "connected to" each other. It often stacks with buzzwords ("widely associated", "particularly associated") and sometimes repeats through a whole paragraph.

Words to watch: associated with, in association with, connected with/to, in connection with.

> AI-flavored: Okafor has been associated with technology leadership at Brightwell Labs.
>
> Specific: Okafor was chief technology officer of Brightwell Labs from 2019 to 2023.

Fix: name the relationship. If the source doesn't say what the relationship was, the sentence isn't supported.

#### Vague attributions and overgeneralized opinion

Weasel wording: "Experts argue", "Observers have noted", "Industry reports suggest", with one source or none behind it. One reviewer becomes "critics"; two articles become "several publications"; "such as" implies a longer list than exists. Sometimes the supposedly independent opinion comes from the subject's own website.

Words to watch: experts argue, observers have cited, some critics argue, industry reports, several sources/publications (when few are cited), widely interpreted/regarded, such as (in front of what is in fact the complete list).

Fix: name who said it or cut it. Match the quantity word to the number of sources.

#### Didactic disclaimers and editorializing

Notes to an imagined reader: "It's important to note that...", "It's crucial to remember...", safety caveats, "may vary by jurisdiction", or careful disambiguation from unrelated things nobody mentioned.

Words to watch: it's important/crucial/critical to note/remember/consider, may vary.

Fix: delete, or turn a real caveat into a plain, sourced statement.

#### Hedging about missing sources, and speculation to fill the gap

When a model can't find information, it says so in the text ("While specific details are limited...", "not widely documented", "based on available information", "in the provided sources"), then guesses what is "likely" true and why that would matter. The guess is invented, and the claim that nothing is documented may be too. Related forms: knowledge-cutoff disclaimers ("as of my last training update"), "as of [date]" statements of absence ("No significant controversies have been documented as of June 2025"), and hedges about how the reader should use the information.

Fix: remove the hedge and the speculation. If information is missing, leave it out or say so plainly where the format calls for it.

#### Section-ending summaries and conclusions

"In summary", "In conclusion", "Overall", a "Conclusion" heading, or a closing sentence that restates the paragraph it ends. Encyclopedic writing, and most professional writing, doesn't do this.

#### Formulaic "challenges" and "future outlook" endings

A rigid outline that ends with "Despite its [praise], X faces several challenges, including..." followed by "Despite these challenges, X continues to thrive..." or speculation about how future initiatives will help. There is often a separate "Future prospects" section. The sign is the formula, not any mention of challenges.

#### Template-like section headings

Headings of the form "X and Y" stack up ("Legacy and influence", "Challenges and legacy", "Sustainability and future challenges"). A heading called "Awards and recognition", or just "Recognition", is nearly universal in AI-generated biographies and company pages, far more than in human-written promotional articles.

#### Treating a list or descriptive title as a named thing

The first sentence defines the title as if it were a real-world entity: "'List of songs about rivers' is a curated compilation of musical works that..." Mostly relevant to wikis and reference works.

### Language and grammar

These patterns appear regardless of topic, which gives AI text a recognizable voice.

#### High density of "AI vocabulary"

Certain words became far more frequent after 2022 and tend to appear together. One or two in a passage mean nothing; many of them, repeatedly, is one of the strongest signals there is. Take the lists literally: a word being overused does not make its synonyms suspect. Watch for literal senses too ("underscore" as a character, or as film music).

General list: additionally (especially opening a sentence), align with, boasts (meaning "has"), bolstered, crucial, deep dive, delve, emphasizing, enduring, enhance, fostering, garner, highlight (as a verb), interplay, intricate/intricacies, landscape (abstract), meticulous/meticulously, pivotal, robust, showcase, tapestry (abstract), testament, underscore (as a verb), valuable, vibrant. Related habit: replacing plain "is" and "has" with "serves as", "stands as", "boasts" or "features".

The favored words shift between model generations. These periods are rough, not hard cutoffs:

| Period | Typical model | Words that cluster |
|---|---|---|
| 2023 to mid-2024 | GPT-4 | additionally, boasts, bolstered, crucial, delve, emphasizing, enduring, garner, intricate/intricacies, interplay, key, landscape, meticulously, pivotal, underscore, tapestry, testament, valuable, vibrant |
| Mid-2024 to mid-2025 | GPT-4o | align with, bolstered, crucial, emphasizing, enhance, enduring, fostering, highlighting, pivotal, showcasing, underscore, vibrant |
| Mid-2025 to mid-2026 | GPT-5 | emphasizing, enhance, highlighting, showcasing, plus the notability and media-coverage phrasing above |
| Mid-2026 on | GPT-6 | challenge, clearer, dependable, echoed, foster, leverage, matters, multifaceted, practical, prioritize, quietly, steady, universally; short sentences of roughly 8 to 20 words, with periods and commas favored over em dashes |

"Delve" peaked in 2023 and early 2024 and dropped sharply in 2025. Each chatbot has its own idiolect: Grok, for example, overuses quasi-scientific words (causal, empirical, correlate) and was still overusing "underscore" in 2026.

#### Negative parallelism

"Not only X but Y", "It's not just X, it's Y", "X isn't merely A; it's B". It can span sentences: "...a family renowned for its theatrical legacy. His life, however, took a different path."

> It's not just a café; it's a living archive of the neighborhood.

#### Outlines of negatives

Strings of short negations that end in a pivot, common in AI-written arguments and comments: "No shortcuts. No compromises. Just results." / "Not a career, not a body of work, just a viral moment."

#### Rule of three

Compulsive triplets of adjectives or parallel phrases, often used to make thin analysis look thorough: "The summit brings together innovators, educators, and changemakers for keynotes, workshops, and networking."

#### Elegant variation

A repetition penalty discourages models from reusing a word, so one person becomes "the researcher", then "the Seoul-born scientist", then "the award-winning academic" in successive sentences. This sign is weaker if the text was assembled from separately generated pieces.

#### False ranges

"From X to Y" where X and Y don't sit on any shared scale: "From ancient philosophy to machine learning, from street food to haute cuisine, ..." Real ranges ("from 1990 to 2000", "from mild to severe") and true merisms ("head to toe") are fine. Test: can you name something in the middle without switching to a different scale?

### Style and formatting

- Title Case in every heading ("Early Life and Education" rather than "Early life and education").
- Mechanical boldface: the same key term bolded on every appearance, "key takeaways" style. Some newer apps instruct models to avoid this.
- Inline-header lists: a bullet or number, a bold label, a colon, then a sentence. When copied as plain text this may show up with literal "•", "–" or "1." characters and lost line breaks.
- Emoji in front of headings or bullet points.
- Em dashes used more often than humans use them in the same genre, in spots where people would use commas, parentheses or colons, often for punchy sales-style emphasis. Useful only together with other signs, and newer models use fewer.
- Curly quotation marks and apostrophes, or a mix of curly and straight in one text. Weak on its own: word processors, phones and professionally typeset sources produce curly quotes too.
- A "Subject:" line at the top of a message meant for a talk page, form or comment box.

### Chatbot leftovers: text meant for the user, not the reader

These are the closest thing to conclusive signs that a chatbot was involved.

- Assistant chatter: "Certainly!", "Of course!", "Here is a draft...", "I hope this helps", "Let me know if you'd like it expanded", "Would you like me to...", "You're absolutely right!", or notes that the text was written "in a neutral, encyclopedic tone following Wikipedia conventions".
- Advice or prewriting pasted as content: "In this section, we will discuss...", suggestions about which images could be added, instructions on how to submit the text.
- Knowledge-cutoff disclaimers: "As of my last knowledge update in January 2022...".
- Refusals: "As an AI language model, I can't...". These have become rare.
- Unfilled templates: "[Entertainer's Name]", "[Describe the specific section that needs editing]", "[URL of reliable source]", and placeholder dates such as "2025-xx-xx" in citation fields.
- Notes about the placeholders themselves: "(Note: the following references are placeholders to indicate where citations would go.)"

### Markup and tool artifacts

- Markdown in a place that uses other markup: "##" headings, "**bold**", "[text](url)" links, triple-backtick fences. Strong when mixed with broken native markup, especially a fence labelled "wikitext". Markdown alone is weak evidence, since many people write it habitually.
- Garbled templates or markup that the writer's tools wouldn't produce.
- ChatGPT citation placeholders such as `citeturn0search0`, `turn0image0`, `citeturn0news0`, with numbers that climb through the text, often wrapped in invisible private-use characters.
- `:contentReference[oaicite:0]{index=0}` and `[oai_citation:0‡example.com](url)`.
- JSON fragments like `({"attribution":{"attributableIndex":"1009-1"}})`.
- `[attached_file:1]` or `[web:1]` at sentence ends (seen since fall 2025, possibly from Perplexity).
- UTM parameters `utm_source=chatgpt.com` (before August 2025) or `utm_source=openai`. These show ChatGPT found the link, not that it wrote the prose; some people use AI only to look up citations.
- "↩" footnote back-arrows carried over from a chat interface.
- `<|endoftext|>`, or text that stops mid-sentence (also caused by bad copy-paste, or a sign of copying from elsewhere).
- Categories or tags that don't exist, and "See also" sections padded with generic links, often exactly three.

To scan a file for the hard artifacts:

```bash
grep -nEi 'turn0(search|image|news|file)[0-9]+|contentReference\[oaicite|oai_citation|attributableIndex|utm_source=(chatgpt\.com|openai)|\[(attached_file|web):[0-9]+\]|<\|endoftext\|>|as an ai language model|as of my last (knowledge|training) update|[0-9]{4}-xx-xx' FILE
```

A hit is strong evidence of chatbot involvement, though it says nothing about how much of the text the chatbot wrote.

### Citations

- Several dead links that were never captured by web archives (Wayback Machine, archive.today). Links rot over time, but a link no archive ever saw probably never existed.
- ISBNs with invalid checksums; DOIs that don't resolve, or resolve to unrelated papers.
- Real-looking books cited without page numbers, so nothing can be checked.
- A real reference that has nothing to do with the claim it supports.
- Impossible details: an author who was dead at the claimed publication date, or a journal issue that contains no such article.
- Broken reference syntax, such as references "reused" incorrectly after every sentence, or named references declared but never used.

On Wikipedia, citations that are fabricated or unrelated to the content are one of the few objective grounds for speedy deletion of LLM-generated pages (criterion G15).

A quick ISBN check:

```python
def isbn_valid(s: str) -> bool:
    d = [c for c in s.upper() if c.isdigit() or c == "X"]
    if len(d) == 10 and "X" not in d[:9]:
        return sum((10 - i) * (10 if c == "X" else int(c)) for i, c in enumerate(d)) % 11 == 0
    if len(d) == 13 and "X" not in d:
        return sum(int(c) * (1 if i % 2 == 0 else 3) for i, c in enumerate(d)) % 10 == 0
    return False
```

### Context and behavior

- A sudden change in one writer's style, such as flawless formal prose from someone whose other messages are casual and loose.
- A mismatch in English variety: American spelling from a writer or on a topic that would normally use British, Indian or another variety. LLMs default to American English unless told otherwise. Only a sudden, complete switch is meaningful; non-native writers often mix varieties.
- Overlong edit summaries, change notes or commit messages written as formal first-person paragraphs that itemize style rules ("refined tone, ensured neutrality, improved clarity and flow"). Very common on Wikipedia as of late 2026.
- Notes addressed to reviewers inside a submission, arguing that it meets the rules.
- On Wikipedia: drafts that arrive with an empty, already-declined Articles for Creation template, apparently added at a chatbot's suggestion.

## Weak indicators: don't rely on these

The guide warns that these are commonly used but ineffective, and some point the other way.

- Perfect grammar. Many people are skilled writers.
- "Bland" or "robotic" prose. Default LLM prose is effusive and verbose, not robotic.
- Fancy, academic or rare words. LLMs overuse a specific set of words; rare words in general are less likely from an LLM, apart from proper nouns tied to the topic.
- Letter-style formatting with greetings and sign-offs, on its own. People wrote that way long before chatbots.
- Connectives like "moreover" and "furthermore", on their own. They are typical of human essay writing too.
- Random-looking markup glitches not listed above. These usually come from editors, browser extensions or translation tools.
- Curly quotes, em dashes or Markdown, each on its own.

## Workflow: reviewing a text

1. Check the date if you can. Pre-December 2022 text is almost certainly not LLM output.
2. Look for hard artifacts first: chatbot leftovers, placeholders and the markup patterns above. Run the grep if the text is in a file.
3. Read for content patterns. Apply the transplant test to suspicious sentences.
4. Tally language patterns and note where they cluster.
5. If there are citations, spot-check them: open some links, confirm the cited source says what the text claims, validate ISBNs and DOIs.
6. Weigh the evidence against the weak indicators and what you know of the writer and context.
7. Report, in this shape:

```markdown
## Assessment
Likelihood of substantial LLM generation: low / moderate / high, with one or two sentences on why.

## Signs found
Grouped by category. For each: the exact passage, the pattern it matches, and how strong a sign it is.

## Problems to fix regardless of origin
Unsupported or unverifiable claims, missing or misattributed sources, puffery, interpretation presented as fact.

## Limits of this review
What you couldn't check, and what would change the assessment.
```

Use calibrated language: "shows several strong signs of", "consistent with", "no strong signs". Avoid "proves" and "definitely written by AI". If only weak indicators turned up, say so plainly.

## Workflow: writing and revising

Aim for what a careful human editor would produce: specific, sourced, plain.

1. Replace the generic with the specific. For each inflated or interpretive sentence, ask what fact it stands in for, and write that fact. If there isn't one, cut the sentence.
2. Don't swap synonyms. Changing "pivotal" to "key" or "highlighting" to "showing" leaves the same empty sentence. The word lists show where to look; the fix is to rewrite or delete.
3. Use plain verbs: "is", "has", "was", rather than "serves as", "stands as", "boasts".
4. Name sources and relationships exactly. Make "several", "critics" and "experts" match the real count.
5. Drop the frame: no opening that announces what the section will do, no closing summary, no challenges-then-bright-future boilerplate, no disclaimers aimed at the reader.
6. Let structure follow content. Not every list has three items, and not every point needs a contrast.
7. Format for the destination: use its markup, sentence-case headings unless the house style says otherwise, bold sparingly, and prose rather than bold-labelled bullet lists.
8. Never invent to fill a gap. If you lack information, leave it out or ask for it rather than writing what is "likely".
9. Remove all chat residue and tool artifacts before delivering.

A fuller before and after:

> Before: Nestled in the heart of the valley, Marlow Creek is a vibrant town that boasts a rich cultural heritage. Founded in 1847, it played a pivotal role in the region's development, reflecting broader trends of westward expansion. Today, the town continues to captivate visitors with its stunning natural beauty, diverse array of local businesses, and enduring sense of community. Despite these strengths, Marlow Creek faces several challenges, including an aging population and limited infrastructure. Nevertheless, ongoing initiatives position it well for a bright future.
>
> After: Marlow Creek is a town of about 3,200 people in the Hadley Valley. It was founded in 1847 as a stop on the Fenwick stagecoach line, and a sawmill built in 1859 was its main employer until it closed in 1961. In the 2020 census the median age of residents was 51, compared with 38 statewide.

The "after" depends on facts the writer actually has. Without facts like these, the honest version is shorter, not vaguer.

Final check before delivering:

- Could any sentence move to an article on another subject unchanged?
- Does anything other than a person "highlight", "underscore", "reflect" or "symbolize" something?
- Are there more than a handful of words from the vocabulary table?
- Any "not just X, it's Y", "No X. No Y. Just Z.", or reflexive triplets?
- Any "it's important to note", "in conclusion" or "despite these challenges"?
- Can every attribution be traced to a specific source that says that?
- Any chatbot residue, placeholders or tool artifacts left?

### When asked to make AI text "pass as human"

Wikipedia's editors specifically ask people not to treat these signs as the problems to fix, because polishing away surface signs while leaving unverified or invented content in place hides the real problem. So apply the whole writing workflow, including checking claims and sources, rather than only removing tells. Where a venue requires disclosure of AI assistance (Wikipedia, many schools, journals and publishers), cleaner prose doesn't change that obligation, and it's worth saying so when relevant.

## Wikipedia-specific notes

Use these only when the work involves Wikipedia.

- The page this skill adapts is an advice page from WikiProject AI Cleanup, not a policy or guideline. For handling suspected LLM content, see Wikipedia:WikiProject AI Cleanup/Guide and Wikipedia:Large language models; for disclosure, WP:LLMDISCLOSE.
- Speedy deletion criterion G15 covers only the most objective signs: chatbot communication addressed to the user, and citations that are fabricated or unrelated to the content. Every other sign here needs discussion or other processes, and a detector score never qualifies.
- Wikipedia uses wikitext, not Markdown. Markdown syntax, or a mix of Markdown and broken wikitext, is the most common formatting sign in new AI-generated drafts.
- Editors can practice with Wikipedia:AI or not quiz.

## Credits and license

This skill adapts "Wikipedia:Signs of AI writing" (https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), an advice page written by WikiProject AI Cleanup and other Wikipedia contributors (history: https://en.wikipedia.org/w/index.php?title=Wikipedia:Signs_of_AI_writing&action=history), licensed under the Creative Commons Attribution-ShareAlike 4.0 International license.

Changes made: the text is condensed and reworded, the material is reorganized into review and writing workflows for use as an agent skill, and all illustrative examples are original rather than drawn from Wikipedia edits. The grep pattern and ISBN snippet are additions. It reflects the page as it stood in October 2026; the original is updated often, so check it for newer patterns.

This adaptation is licensed under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/).
