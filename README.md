## Carlos Tapia

Software architect and technical lead. Thirteen years on systems that other people
depend on — banking, telecommunications, public sector. Event-driven architecture,
microservices, and the kind of legacy migration where the old platform cannot be
switched off while you replace it.

For the past year I've been running teams of AI agents against my own production
systems and measuring what happens — 5,605 turns logged and priced one by one, as
of September 2026. Not benchmarks: real repositories, where the task isn't curated
and someone has to verify the result before it counts.

**I publish the measurements, including the ones that went against what I expected.**

---

### What I'm working on

**[seisin](https://github.com/carlostapiacl/seisin)** · a permission layer
for AI coding agents. Give each agent its own folders and its own keys, and when the
kernel blocks something, it tells you *whose* file it was. It is not a sandbox — it
sits on top of one. The isolation comes from the OS; what seisin adds is the part an
OS cannot know: which role a path belongs to, and therefore who to ask next.
`MIT` · [npm](https://www.npmjs.com/package/seisin)

**[audio-booster](https://github.com/carlostapiacl/audio-booster)** ·
volume boost for macOS without a driver. Uses `AudioHardwareCreateProcessTap` instead
of the HAL driver every other tool installs, so it never asks for sudo and never
hijacks your default output. `MIT` · Swift

---

### Some things I measured

| | |
|---|---|
| Resetting an agent's thread every turn cost **25% more**, not less | the cache rebuild is the hidden line item |
| Compaction only pays above **~17 remaining tool calls** | and that number is unknowable when you have to decide |
| Cost tracks **tool calls per turn**, not team size | so splitting a large team doesn't fix it |
| Of 16 layers in an agent stack, **3 have a settled standard** | sandboxing, identity and authorisation are not among them |

Each one has the experiment, the sample and the source behind it →
**[carlostapia.cl](https://carlostapia.cl)**

---

### Elsewhere

[carlostapia.cl](https://carlostapia.cl) · notes and measurements &nbsp;·&nbsp;
[LinkedIn](https://www.linkedin.com/in/carlostapiaolguin)
