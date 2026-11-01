# Signs of AI writing (Claude skill)

A skill that teaches Claude to spot the habits of AI-generated text and to write without them. It is based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), the field guide maintained by Wikipedia's WikiProject AI Cleanup.

With the skill installed, Claude can:

- review a piece of text and report which signs of AI generation it shows, how strong they are, and what to check next
- revise a draft so it is specific and sourced instead of generic and inflated
- scan a file for leftover chatbot artifacts such as `turn0search0` or `utm_source=chatgpt.com`

These signs are clues, not proof. Human writers share many of the same habits, and the skill tells Claude to say so.

## Install in Claude Code

### Easiest: let Claude Code do it

Start Claude Code and paste this request:

```
Install the skill from https://github.com/qzxcle/signs-of-ai-writing-skill as a personal skill: copy its signs-of-ai-writing folder into ~/.claude/skills/
```

### By hand, with git

1. Clone this repo:

   ```bash
   git clone https://github.com/qzxcle/signs-of-ai-writing-skill.git
   ```

2. Copy the skill folder into your personal skills folder.

   macOS or Linux:

   ```bash
   mkdir -p ~/.claude/skills
   cp -r signs-of-ai-writing-skill/signs-of-ai-writing ~/.claude/skills/
   ```

   Windows (PowerShell):

   ```powershell
   New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
   Copy-Item -Recurse "signs-of-ai-writing-skill\signs-of-ai-writing" "$HOME\.claude\skills\"
   ```

### By hand, without git

1. Click the green **Code** button on this page and choose **Download ZIP**.
2. Unzip it. You get a folder called `signs-of-ai-writing-skill-main`.
3. Copy the `signs-of-ai-writing` folder from inside it into your skills folder.

   macOS (assuming the download is in your Downloads folder):

   ```bash
   mkdir -p ~/.claude/skills
   cp -r ~/Downloads/signs-of-ai-writing-skill-main/signs-of-ai-writing ~/.claude/skills/
   ```

   Windows: paste `%USERPROFILE%\.claude\skills` into the File Explorer address bar (create the `skills` folder if it doesn't exist), then copy the `signs-of-ai-writing` folder there.

### Check that it worked

Start Claude Code and type `/`. You should see `signs-of-ai-writing` in the list.

To use the skill in one project only, put the folder in that project's `.claude/skills/` folder instead of your personal one.

## Install in the Claude app (web or desktop)

1. Click the green **Code** button on this page and choose **Download ZIP**.
2. Unzip it. Inside the `signs-of-ai-writing-skill-main` folder you will find a folder called `signs-of-ai-writing`.
3. Compress just that folder into its own ZIP file (on a Mac: right-click, Compress; on Windows: right-click, Send to, Compressed (zipped) folder).
4. In Claude, go to **Customize > Skills**, click **+**, then **Create skill > Upload a skill**, and choose the ZIP from step 3.

Skills need code execution to be turned on in your Claude settings.

## Use it

Ask in plain language and Claude uses the skill when the request fits:

- "Does this read like it was written by AI?" (then paste the text)
- "Check draft.md for AI tells and tell me what to fix."
- "Rewrite this paragraph so it's specific instead of generic."

In Claude Code you can also call it directly with `/signs-of-ai-writing`.

## Update or remove

To update after a new version is published, get the latest files and replace the old folder.

macOS or Linux:

```bash
cd signs-of-ai-writing-skill
git pull
rm -rf ~/.claude/skills/signs-of-ai-writing
cp -r signs-of-ai-writing ~/.claude/skills/
```

Windows (PowerShell):

```powershell
cd signs-of-ai-writing-skill
git pull
Remove-Item -Recurse -Force "$HOME\.claude\skills\signs-of-ai-writing"
Copy-Item -Recurse "signs-of-ai-writing" "$HOME\.claude\skills\"
```

To remove it, delete the `signs-of-ai-writing` folder from `~/.claude/skills/`. In the Claude app, go to **Customize > Skills**, open the skill, and delete it from the **...** menu.

## What's in this repo

```
README.md                 this file
LICENSE                   CC BY-SA 4.0
signs-of-ai-writing/
└── SKILL.md              the skill
```

The skill is a single Markdown file of instructions. It has no dependencies and needs no API keys or accounts. It includes a short `grep` command and a small Python function (an ISBN checker) that Claude may run while reviewing text.

## Credits and license

The skill adapts [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) by WikiProject AI Cleanup and other Wikipedia contributors, published under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). The text has been condensed, reworded and reorganized for use as a Claude skill, and the examples are original.

This repository is licensed under CC BY-SA 4.0 as well. If you share a modified version, credit the sources and use the same license.

The skill reflects the Wikipedia page as of October 2026. The page changes often, so check the original for newer patterns.

This is a community project. It is not affiliated with Wikipedia, the Wikimedia Foundation or Anthropic.
