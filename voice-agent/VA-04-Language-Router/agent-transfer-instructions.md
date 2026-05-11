# Agent Transfer Setup — VA-04: Language Router

> GHL → Settings → Voice AI → VA-04: Language Router → Actions
> Add 3 Agent Transfer actions — one per language agent.

---

## How Agent Transfer Works in GHL

In the Voice AI agent, add an **Agent Transfer** action for each target agent. Each action has a **"When to transfer to this agent"** field — this is the trigger instruction that tells the router WHEN to fire that specific transfer.

The router agent reads the caller's reply to the welcome message, matches it against the transfer conditions, and fires the correct transfer immediately.

---

## Action 1 — Transfer to English Agent

**Action type:** Agent Transfer
**Select agent:** VA-01: English — Sonu da Dhaba

**When to transfer to this agent:**
```
Transfer to this agent when the caller says "English", responds in English, or clearly indicates they want to speak in English.
```

---

## Action 2 — Transfer to Hindi Agent

**Action type:** Agent Transfer
**Select agent:** VA-02: Hindi — Sonu da Dhaba

**When to transfer to this agent:**
```
Transfer to this agent when the caller says "Hindi", responds in Hindi, or clearly indicates they want to speak in Hindi.
```

---

## Action 3 — Transfer to Punjabi Agent

**Action type:** Agent Transfer
**Select agent:** VA-03: Punjabi — Sonu da Dhaba

**When to transfer to this agent:**
```
Transfer to this agent when the caller says "Punjabi", responds in Punjabi, or clearly indicates they want to speak in Punjabi.
```

---

## Important Setup Notes

**Phone number connects to VA-04 only.** VA-01, VA-02, and VA-03 are never connected to the phone number directly — they only receive transferred calls from the router.

**KB not needed on VA-04.** The router agent does not answer questions and has no ordering capability, so it does not need the knowledge base attached. Attach KB-01 only to VA-01, VA-02, and VA-03.

**All 3 transfers must be saved before going live.** If a transfer action is missing, callers saying that language will get stuck with the router indefinitely.

**Test each path before going live:**
- Call in and say "English" → should land on VA-01 within 2 seconds
- Call in and say "Hindi" → should land on VA-02 within 2 seconds
- Call in and say "Punjabi" → should land on VA-03 within 2 seconds
- Call in and say nothing / say something unrecognised → router should ask once more, then end gracefully

---

## GHL Agent Naming Convention

| GHL Agent Name | Role |
|----------------|------|
| VA-01: English — Sonu da Dhaba | English ordering agent |
| VA-02: Hindi — Sonu da Dhaba | Hindi ordering agent |
| VA-03: Punjabi — Sonu da Dhaba | Punjabi ordering agent |
| VA-04: Language Router — Sonu da Dhaba | Entry point — routes all inbound calls |
