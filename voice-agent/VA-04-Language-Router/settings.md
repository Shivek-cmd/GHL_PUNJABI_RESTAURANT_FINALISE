# Technical Settings — VA-04: Language Router — Sonu da Dhaba

> GHL → Settings → Voice AI → VA-04: Language Router — Sonu da Dhaba
> This agent only routes calls — keep settings minimal and fast.

---

## Call Settings

| Setting | Value |
|---------|-------|
| Max Call Time | `2 minutes` | 
| End Call After Silence | `10 seconds` |
| Wait Before Speaking | `0.1 seconds` |

> Max 2 minutes — this agent should never be on a call longer than 30 seconds. If it is, something is wrong.

### Idle Reminders
| Setting | Value |
|---------|-------|
| Enable | ON |
| Starts After | `4 seconds` silence |
| Repeat | `2 times` |

Reminder 1: `"Hey, are you still there? — Haan, kya aap sunne ho? — Haan, ki tusi sunne ho?"`
Reminder 2: `"No problem — give us a call back when you're ready. Bye!"`

---

## Agent Behaviour

| Setting | Value |
|---------|-------|
| Response Speed | `0.9` |
| Interruption Sensitivity | `0.60` |
| LLM Temperature | `0.2` |

> Response Speed `0.9` — faster than the order agents. This agent just needs to detect a word and transfer. Lower temperature `0.2` keeps it consistent and prevents it from going off-script.

### Backchannel
| Setting | Value |
|---------|-------|
| Enable | OFF |

> No backchannel needed — this agent's turn is just a few seconds long.

---

## Transcription & Speech

| Setting | Value |
|---------|-------|
| Transcription Model | `Fast` |
| Vocabulary Specialisation | `General` |

### Boosted Keywords
```
English, Hindi, Punjabi, Haan ji, yes, no
```

> Minimal keywords — the router only needs to recognise the three language names and basic yes/no.

### Pronunciation Dictionary
> None needed — the router speaks very little and only uses simple English words.

---

## Voice Settings

| Setting | Value |
|---------|-------|
| Noise Cancellation | `Remove Noise` |
| Background Sound | `None` |
| Voice Speed | `1.0` |
| Voice Temperature | `0.5` |
| Voice Volume | `1.0` |
| Speech Normalization | OFF |
| Dynamic Voice Speed | OFF |

> Speech Normalization and Dynamic Voice Speed both OFF — this agent says one sentence and transfers. No prices, no times, no adaptive pacing needed.
