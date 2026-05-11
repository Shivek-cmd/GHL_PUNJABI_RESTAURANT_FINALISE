# Sonu da Dhaba — GHL Voice AI Technical Settings

> Configure these in GHL → Settings → Voice AI → your agent. Tuned for a multilingual restaurant ordering call (English, Hindi, Punjabi) with Indian food names.

---

## Latency Fix Guide

> **If you're getting 3–4 second delays**, work through this list in order.

| Layer | Cause | Fix |
|-------|-------|-----|
| **STT** | Accurate model adds 1–2s per turn | Switch to Fast + boosted keywords |
| **LLM** | Long prompt = slower inference | Keep prompt under 900 words |
| **TTS** | Long responses = more audio to render | Keep agent sentences short |
| **GHL** | Wait Before Speaking too high | Reduce to 0.1s |
| **Response Speed** | Set too low | Increase to 0.8 |

**Do these first:**
1. Transcription model: Accurate → **Fast**
2. Wait Before Speaking: 0.5s → **0.1s**
3. Response Speed: 0.65 → **0.8**

---

## 1. Call Settings

| Setting | Value | Reason |
|---------|-------|--------|
| **Max Call Time** | `8 minutes` | Restaurant calls rarely exceed 5 min. 8 min covers long orders and chatty callers. |
| **End Call After Silence** | `15 seconds` | If caller goes completely silent after all reminders, end the call gracefully. |
| **Wait Before Speaking** | `0.1 seconds` | Major latency fix. 0.1s still sounds natural; 0.5s adds dead air every single turn. |

### Idle Time Reminder

| Setting | Value |
|---------|-------|
| **Enable** | ON |
| **When Reminder Starts** | `5 seconds` of silence |
| **How Often They Repeat** | `3 times` |

**Reminder messages — set all three (agent matches language automatically):**

> Reminder 1: "Hey, are you still there? — Haan, kya aap sunne ho? — Haan, ki tusi sunne ho?"
> Reminder 2: "Just checking — did you want to continue? — Kya aap continue karna chahte ho? — Ki tusi continue karna chahunde ho?"
> Reminder 3: "I'll go ahead and end the call if you're done. Thanks for calling Sonu da Dhaba! — Theek hai, call band karta hoon. Shukriya! — Theek hai, call band karda haan. Shukriya!"

---

## 2. Agent Behaviour

| Setting | Value | Reason |
|---------|-------|--------|
| **Response Speed** | `0.8` | Faster generation. Restaurant callers expect quick replies — lower values add noticeable delay. |
| **Interruption Sensitivity** | `0.60` | Mid-range — callers often jump in. This lets them cut in naturally without false triggers from background noise. |
| **LLM Temperature** | `0.3` | Low = consistent, predictable. Critical for order-taking — you don't want creative variation when confirming items. |

### Backchannel

| Setting | Value |
|---------|-------|
| **Enable Backchannel** | ON |
| **Backchannel Frequency** | `0.4` |
| **Backchannel Word List** | See below |

**Backchannel words (covers all three languages — paste as comma-separated):**
```
Got it, Sure, Okay, Mhm, Yeah, Right, Yep, Haan ji, Theek hai, Bilkul, Acha, Ji haan, Haan, Zaroor
```

> Backchannel makes Preet sound like she's actively listening while the caller speaks. Keep frequency at 0.4 — too high sounds annoying, too low sounds robotic.

---

## 3. Transcription & Speech

### Transcription Model
**Select: Fast**

> Accurate adds 1–2 seconds per turn — too slow for a live phone call. Fast with boosted keywords handles Indian food names well. If a specific item still gets misheard, add it as a boosted keyword. If accuracy is unacceptable on Fast, switch back to Accurate and accept the latency.

### Vocabulary Specialisation
**Select: General**

> General handles English + Indian food names in romanized form. Medical is not relevant here.

### Boosted Keywords

**Max 50 — prioritised for STT failure risk (Indian food names TTS struggles with most).**
Common English words (mild, medium, delivery) don't need boosting — STT handles them fine.

```
Samosa, Pakora, Paneer Tikka, Seekh Kebab, Amritsari,
Papdi Chaat, Golgappa, Pani Puri,
Tandoori Roti, Kulcha, Bhatura, Aloo Paratha, Gobi Paratha,
Paneer Paratha, Makki di Roti,
Dal Makhani, Dal Tadka, Chana Masala, Rajma, Kali Dal,
Paneer Butter Masala, Palak Paneer, Kadai Paneer, Shahi Paneer,
Murgh Makhani, Kadai Chicken, Chicken Rogan Josh, Chicken Karahi,
Mutton Rogan Josh, Mutton Karahi, Mutton Keema, Mutton Korma, Bhuna Gosht,
Aloo Gobi, Bhindi Masala, Baingan Bharta, Sarson da Saag,
Biryani, Jeera Rice,
Raita, Boondi Raita, Papad, Nimbu Pani, Masala Chai,
Lassi, Gulab Jamun, Gajar ka Halwa, Kulfi, Ras Malai
```

> **50 keywords exactly.** If a specific item still gets misheard after go-live, swap out a lower-risk entry for it.

### Pronunciation Dictionary

**Max 20 — picked for highest TTS failure risk. These are the words an English TTS engine will most badly mispronounce without correction.**

| Word | Pronunciation (paste into GHL) |
|------|-------------------------------|
| Dal | dahl |
| Paneer | puh-NEER |
| Makhani | muh-KAH-nee |
| Paratha | puh-RAH-tah |
| Bhatura | buh-TOO-rah |
| Raita | RYE-tah |
| Biryani | bir-YAH-nee |
| Masala | muh-SAH-lah |
| Lassi | LUS-see |
| Naan | nahn |
| Chai | chye |
| Gulab Jamun | goo-LAHB juh-MOON |
| Kulfi | KOOL-fee |
| Halwa | HUL-wah |
| Tandoori | tan-DOO-ree |
| Seekh | seek |
| Chana | CHAH-nah |
| Sarson | SAR-son |
| Pakora | puh-KOH-rah |
| Rogan Josh | ROH-gun josh |

---

## 4. Voice Settings

### Noise Cancellation
**Select: Remove Noise**

> Callers may be in kitchens, cars, or noisy environments. "Remove Noise" handles this without stripping the caller's voice like "Remove Noise + Background Speech" can.

### Background Sound
**Select: None**

> Clean line sounds more professional for a dhaba order call.

### Voice Levels

| Setting | Value | Reason |
|---------|-------|--------|
| **Voice Speed** | `1.0` | Default natural speed. Let Dynamic Voice Speed adjust for slower callers. |
| **Voice Temperature** | `0.65` | Slightly expressive — Preet is warm, not flat. Don't go above 0.8 or responses sound inconsistent. |
| **Voice Volume** | `1.0` | Default. Adjust only if testers report it too quiet or too loud. |

### Toggles

| Setting | Value | Reason |
|---------|-------|--------|
| **Speech Normalization** | ON | Converts `$13.99` → "thirteen ninety-nine", `7:30 PM` → "seven thirty PM". Essential for order recaps. |
| **Dynamic Voice Speed** | ON | Automatically slows for callers who speak slowly. Feels natural — important for elderly callers or those less familiar with English. |

---

## 5. Voice Selection Note

> When choosing the TTS voice in GHL, pick a voice that handles romanized Hindi/Punjabi words reasonably well. Test by having it say: "Dal Makhani", "Sarson da Saag", "Gulab Jamun", and "Haan ji" — if it sounds natural, it's a good match. The pronunciation dictionary above corrects the most common errors regardless of which voice you pick.

---

*End of Technical Settings — Sonu da Dhaba | Preet*
