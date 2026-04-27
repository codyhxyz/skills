# codyhxyz-plugins 🍋
These days I talk to my computer more than I use the keyboard and mouse. We've entered a new dawn of human-computer interaction where individuals' computer use is starting to diverge. If 2025 was the Year of the Agent, 2026 the start to the era of '[Bespoke Software](https://x.com/karpathy/status/2024583544157458452)'.

In the spirit of open-sourcing myself, I'm open-sourcing my Claude plugins. The gap between individuals who are augmenting themselves and those who aren't is growing. When I find a way of working with the computer that works for me, I want to share that experience. This is my contribution bridge that gap. 

Less is more. As the cost of software development approaches $0, it's getting harder to see the signal through the noise. I publish here when what I build passes the "You-Aren't-Gonna-Need-It" check. This is my contribution to increase the Signal-to-Noise Ratio.

These are the tools I use to interact with the digital world. This is my bespoke interface.

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://claude.com/product/claude-code"><img src="https://img.shields.io/badge/built_for-Claude%20Code-d97706" alt="Built for Claude Code"></a>
</p>

<p align="center"><img src="assets/hero.svg" alt="codyhxyz-plugins · for those who need the lemon zest" width="100%"></p>

## install

add the marketplace and install any plugin from the table below in one go:

```
/plugin marketplace add codyhxyz/codyhxyz-plugins && /plugin install <plugin-name>@codyhxyz-plugins
```

pull new plugins and version bumps manually:

```
/plugin marketplace update codyhxyz-plugins
```

## important! enable auto-update

third-party marketplaces ship with auto-update **off** by default (a questionable default — see below). turn it on so you get version bumps without thinking about it:

1. run `/plugin` in Claude Code
2. open the **Marketplaces** tab
3. select `codyhxyz-plugins` → **Enable auto-update**

or set it in `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "codyhxyz-plugins": {
      "source": { "source": "github", "repo": "codyhxyz/codyhxyz-plugins" },
      "autoUpdate": true
    }
  }
}
```

## available plugins

### shipping software

| Plugin | What it does |
|---|---|
| [`create-claude-plugin` 🛠️](https://github.com/codyhxyz/create-claude-plugin) | A claude plugin that ships claude plugins. Scaffold it, validate it, push it, submit it to the official Anthropic marketplace, all in one session. Makes your plugins look gooood on GitHub + elsewhere. |
| [`create-chrome-extension` 🧩](https://github.com/codyhxyz/create-chrome-extension) | Six skills + a WXT factory that take you from Chrome extension idea to live on the Web Store in one Claude session. Encodes ~18 Chrome Web Store rules as validators so you can't accidentally ship a half-baked listing. |

### coding tools

| Plugin | What it does |
|---|---|
| [`prompt-optimizer` 🎯](https://github.com/codyhxyz/prompt-optimizer) | Bad prompting poisons your context. This plugin fills in the implicit details in your vague prompt. Cuts token use and gets better results in the critical first conversational turn with Opus 4.7. |
| [`first-principles-review` 🔬](https://github.com/codyhxyz/first-principles-review) | A better code review. Use after one-shotting a project, when you want to make sure Claude built what you wanted it to. Scope creep killer. |
| [`eureka` ⚡](https://github.com/codyhxyz/eureka) | A subagent for when claude is trying all the wrong things. Use it when you need Claude to think outside the box. This is my #1 most helpful plugin for unblocking stuck coding sessions. 💡 |
| [`high-agency-mode` 🙅](https://github.com/codyhxyz/high-agency-mode) | Stop hook that catches "can't"/"cannot" in Claude's replies and forces a four-move reframe — name the constraint, list what IS possible, surface tradeoffs, recommend one. Chief-of-staff posture, not refusal posture. _a.k.a. never-say-never, yes-can-do, you-can-just-do-things._ |

### writing

| Plugin | What it does |
|---|---|
| [`synonymmer` 📚](https://github.com/codyhxyz/synonymmer) | Thesaurus on steroids for naming and writing. Outputs 100-200 latent-space-near words and phrases related to your seed term, organized into clusters. |
| [`humanizer` ✍️ ↗](https://github.com/blader/humanizer) | **↗ not mine, just rec'd.** Strips AI tells from text — em-dash overuse, inflated adjectives, filler phrases, the whole "signs of AI writing" checklist. Runs a second pass to catch its own lingering AI-isms, and can voice-match from a writing sample so the output sounds like *you*, not like a cleaned-up LLM. |

### design

| Plugin | What it does |
|---|---|
| [`font-pirate` 🔤](https://github.com/codyhxyz/font-pirate) | All fonts are free now. |
| [`frontend-design` 🎨 ↗](https://github.com/anthropics/claude-code/tree/main/plugins/frontend-design) | **↗ not mine, just rec'd.** Anthropic's own plugin for generating distinctive, production-grade UI — the antidote to default-Tailwind AI slop. Pair with `font-pirate` when you need the typography to match. Install: `/plugin marketplace add anthropics/claude-code && /plugin install frontend-design@claude-code-plugins`. |

### token use reduction

| Plugin | What it does |
|---|---|
| [`statusline` 📊](https://github.com/codyhxyz/statusline) | A Claude Code statusline with HSL-gradient ring meters for context window and 5h/7d rate limits with live reset countdowns. Catch context rot before Anthropic tells you to `/clear`. |
| [`rtk` 🦀 ↗](https://www.rtk-ai.app/) | **↗ not mine, just rec'd.** CLI proxy that transparently rewrites dev commands (git, npm, etc.) to token-optimized equivalents. 60–90% savings on routine tool output — Claude sees filtered summaries instead of raw dumps. |
| [`context-mode` 🪟 ↗](https://github.com/mksglu/context-mode) | **↗ not mine, just rec'd.** MCP server that sandboxes bash/code execution and keeps large outputs out of your context window. Pairs an FTS5 knowledge base with BM25 ranking so you can query past tool output instead of re-reading it. |
| [`caveman` 🪨 ↗](https://github.com/JuliusBrussee/caveman) | **↗ not mine, just rec'd.** Ultra-compressed communication mode. Cuts output tokens ~75% by talking like a caveman while preserving full technical accuracy. Lite / full / ultra intensity. |
| `claude --system-prompt "☯️"` | Zen mode. Skip Claude Code's default system prompt by overriding it with a single symbol. Lower per-turn overhead for quick one-shot queries where you don't need the full tool preamble. |

### interaction

| Plugin | What it does |
|---|---|
| [`hook-sounds` 🔊](https://github.com/codyhxyz/hook-sounds) | Customizable Claude Code notification sound setup via hooks. Ships with an Oddworld: Munch's Oddysee pack by default — dumb, joyful. Swap in your own CC0 sounds if you'd rather. macOS only. |
| **Mobile push notifications, on by default** | Flip `push-to-mobile` from off → on so Claude can wake your phone when it's waiting on you — long-running commands, blocked decisions, review gates. Requires the Claude mobile app. |
| **Remote control, on by default** | Flip the default so every Claude Code session is reachable from the mobile app. Steer runs from anywhere without having to be at the laptop. |
| **Phone-notify stop hook** | A Stop hook that asks Claude, *"should I page you on mobile?"* — fires on long commands (>30s) or when blocked on a decision, skips trivial turns. Prevents the "push for every turn" spam you'd get from an always-on notifier. |

### in development

*zesting, testing, breaking things.*

| Plugin | What it does |
|---|---|
| `pre-mortem` 🔮 | Before executing a plan, imagine it has already failed. Enumerate the most likely failure modes — wrong assumptions, brittle dependencies, ambiguous requirements, silent edge cases, integration seams, retry/rollback gaps — rank by likelihood × blast radius, and fold the cheapest precondition checks into the plan *before* execution starts. _"What would make me wish I'd thought about this for five more minutes?" — answered before the five minutes become five hours._ |
| `post-mortem` 🩹 | After something goes wrong, reconstruct *why*. Separate the proximate cause (the bad line) from the systemic cause (the missing guardrail, the workflow gap that let it through). Capture what was believed vs. what was true, what signal was ignored, and the smallest durable change — a check, a skill, a doc, a hook — that would have caught it. _Turn each scar into a callus._ |
| `strawman/steelman` 🥊 | A confidence stress-test for whatever Claude is asserting. Force it to construct both the *steelman* (the strongest, most charitable version of the opposing view) and the *strawman* (the weakest, most caricatured version), then locate its actual claim against both. Surfaces overconfidence, hidden assumptions, and the cases where Claude is busy demolishing a position nobody actually holds. _If you can't beat the steelman, you don't get to celebrate beating the strawman._ |

## license

[MIT](LICENSE) © 2026 Cody Hergenroeder

---

<sub><i>"i create because i envision that there are people out there who need the lemon zest."</i></sub>
