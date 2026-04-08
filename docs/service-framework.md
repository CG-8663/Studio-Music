# Major 72 Studio — Service Framework

> Defined: 2026-04-08 | Status: Approved direction | Source: Party Mode strategy session

---

## Service Philosophy

Major 72 Studio is not an "AI music generator." It is a **professional production service** powered by AI and guided by human creative judgment. The service promise: take a creator's raw musical idea and elevate it through the lens of an experienced producer's taste.

**Core positioning:** "Your music. Eddie's ears. Nothing added. Everything elevated."

In a market split between "fast and cheap" (Suno) and "slow and expensive" (Songfinch), Major 72 is **fast AND professional** — collapsing the timeline from weeks to minutes while maintaining studio-grade quality.

---

## Four-Tier Service Model

### Hear It — "Upload your idea, hear it polished"

**Price:** $29-49/month subscription
**Phase:** MVP (launch)
**Promise:** Upload any rough recording. Get it back professionally mixed and mastered in Eddie's signature sound. Under 60 seconds.

**What it does:**
- Ingests any audio file (WAV, MP3, FLAC, M4A, AIFF)
- Analyzes key, tempo, genre, energy automatically
- Separates stems (isolates what's there: vocals, bass, guitar, etc.)
- Applies Eddie Signature Creative Mode (frequency balance, dynamics, spatial positioning, tonal character)
- Mixes and masters to mode specification

**What it delivers:**
- Polished stereo mix
- Individual stems
- Before/after comparison
- Session metadata (key, BPM, genre detection)

**What it does NOT do:**
- No arrangement — doesn't add instruments
- No generation — doesn't create new musical content
- No lyrics — works only with what you upload

**Why this works:** The #1 fear among producers is losing creative identity. "Hear It" doesn't change what you wrote — it makes it sound like you spent six hours mixing in a world-class studio. This is the trust builder that converts the cautious experimenter segment.

**Pricing logic:**
- Free tier: 2 tracks/month with watermark
- Pro: Unlimited tracks, stem export, all Creative Modes (as added)
- Replaces 2-3 existing tool subscriptions ($15-40/month each)

---

### Build It — "Full arrangement and production"

**Price:** $79-149/track
**Phase:** Phase 2 (after Hear It proves demand)
**Promise:** Take your polished stems and build a full arrangement with AI Session Players — drums, bass, keys — that follow your chord progressions and match your Creative Mode.

**Prerequisites:** Core engine proven via Hear It; Session Players and arrangement engine built.

**Trigger to build:** Hear It users actively requesting "I love how this sounds, but I need drums and keys."

---

### Play It — "Stage-ready with charts and musicians"

**Price:** $299-999/project
**Phase:** Phase 3
**Promise:** Convert your produced track into professional performance materials — sheet music, click tracks, rehearsal packages — and hire session musicians to record live parts.

**Deliverables:**
- Instrument-specific charts (drums, bass, keys, guitar)
- Tempo maps and click tracks for live sync
- Performance guides and rehearsal documentation
- Sheet music in MusicXML, PDF, or MIDI
- Session musician coordination (via SoundBetter or proprietary network)

**Prerequisites:** Build It operational; score generation engine; marketplace integration.

**Trigger to build:** Build It users asking "My band wants to play this live."

---

### Gift It — "Custom song from your story"

**Price:** $49-149/song (one-time transaction)
**Phase:** Soft-launch alongside Hear It MVP
**Promise:** Record a voice note or write your story. Choose a mood. Get a full, professionally produced song in minutes — not weeks.

**Target market:** Weddings, birthdays, anniversaries, memorials. Non-musicians buying emotional gifts.

**Competitive advantage vs. Songfinch:**
- Songfinch: $199-399/song, 7-14 day delivery, 100% human
- Gift It: $49-149/song, delivery in minutes, AI + Eddie's Creative Mode
- 50-75% cheaper, 1000x faster

**Critical design point:** Gift It must be a **separate brand and landing page** from the professional tool. Same engine, different front door. Don't confuse "professional production platform" with "wedding song generator."

**Growth driver:** 90% of recipients say a custom song is the "most meaningful gift ever." Every song shared on social media is a free ad.

---

## Service Ladder (Land and Expand)

```
HEAR IT ($29-49/mo)          ← LAND: Low friction, proves the magic
    ↓ "I love how this sounds, but I need drums and keys"
BUILD IT ($79-149/track)     ← EXPAND: Higher spend, per-project
    ↓ "My band wants to play this live on Saturday"
PLAY IT ($299-999/project)   ← PREMIUM: High-touch, high-margin
    ↓ Meanwhile, a bride finds you on Google...
GIFT IT ($49-149/song)       ← VOLUME: Separate funnel, emotional purchase
```

Each tier validates the next. Don't build the next tier until users of the current tier are asking for it. **Demand pulls you forward.**

---

## Shared Core Engine

All four tiers share the same production engine:

```
┌──────────────────────────────────────────────┐
│           CORE ENGINE (shared)               │
│  Stem Separation → Creative Mode → Mix/Master│
└──────────┬───────────┬──────────┬────────────┘
           │           │          │
     ┌─────┴──┐  ┌─────┴───┐ ┌───┴─────┐  ┌────────┐
     │ HEAR IT│  │ BUILD IT│ │ PLAY IT │  │ GIFT IT│
     │ Polish │  │ Arrange │ │ Charts  │  │ Create │
     │ only   │  │ + mix   │ │ + hire  │  │ + gift │
     └────────┘  └─────────┘ └─────────┘  └────────┘
```

Build the core engine right for Hear It, and every subsequent tier is an **extension**, not a rebuild.

---

## Year 1 Revenue Targets

| Tier | Target | Avg Revenue | Annual Revenue |
|---|---|---|---|
| Hear It | 1,000 subscribers | $39/mo | $468K |
| Gift It | 2,000 songs sold | $99/song | $198K |
| **Year 1 Total** | | | **~$666K** |

---

## "Hear It" MVP — User Experience

1. **Upload** — Drag and drop. No forms, no genre selection. System auto-detects everything.
2. **Choose Your Sound** — "Polish with Eddie's Signature Sound" (single button at launch)
3. **The Wait** — 30-60 seconds. Show waveform being sculpted. Brief notes on what Eddie's mode is doing.
4. **The Reveal** — Split-screen before/after. One-click toggle. This is the "oh my god" moment.
5. **Download** — Polished mix, stems, session metadata. One zip. Done.

**Total time from landing to files in hand: under 2 minutes.**
