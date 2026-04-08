# Major 72 Studio — Technical Specifications

> Actionable specs broken down by system component, with priorities and dependencies.

---

## System Overview

Major 72 Studio is composed of **6 core systems** that build on each other in layers:

```
┌─────────────────────────────────────────────────┐
│  6. Marketplace & Licensing Layer               │
├─────────────────────────────────────────────────┤
│  5. Blockchain Royalty Infrastructure           │
├─────────────────────────────────────────────────┤
│  4. Consumer Personalization Layer              │
├─────────────────────────────────────────────────┤
│  3. Live Integration & Session Layer            │
├─────────────────────────────────────────────────┤
│  2. Creative Mode Architecture                  │
├─────────────────────────────────────────────────┤
│  1. Core Production Engine (GAW)                │
└─────────────────────────────────────────────────┘
```

---

## SPEC-01: Core Production Engine (GAW)

**Priority:** P0 — Foundation  
**Dependencies:** None (base layer)

### 1.1 Stem Separation Pipeline

| Requirement | Target | Notes |
|---|---|---|
| Max stems extracted | 12+ | Comparable to Lalals (23), prioritize quality over count |
| Processing time | < 60 seconds | For a 3.5-minute track |
| Model architecture | Band-split U-Net variant | Moises-Light reference implementation |
| Compute | Cloud GPU (A100/H100) | Latent diffusion for fast separation |
| Output formats | WAV (48kHz/24bit), FLAC, MP3 | Per-stem exports |

**Actionable Tasks:**
- [ ] Evaluate and benchmark open-source separation models (Demucs v4, HTDemucs, Band-split RNN)
- [ ] Define stem taxonomy (drums, bass, vocals, keys, guitars, strings, woodwinds, FX, etc.)
- [ ] Build cloud inference pipeline with auto-scaling
- [ ] Implement quality scoring — SNR/SDR metrics per stem
- [ ] Build upload ingestion service (accept WAV, MP3, FLAC, M4A, AIFF)

### 1.2 Automated Mixing Engine

| Requirement | Target |
|---|---|
| Frequency analysis | Per-stem spectral profiling |
| Dynamic processing | Adaptive compression/limiting per Creative Mode |
| Spatial processing | Stereo width, panning, reverb per genre context |
| Reference matching | A/B comparison against mode-specific reference tracks |

**Actionable Tasks:**
- [ ] Define mixing signal chain templates per Creative Mode
- [ ] Implement frequency balance analyzer (EQ curve matching)
- [ ] Build dynamic range processor (mode-aware compression ratios)
- [ ] Implement stereo imaging module
- [ ] Create reference track comparison engine (spectral + loudness matching)

### 1.3 Automated Mastering

**Actionable Tasks:**
- [ ] Implement loudness normalization (LUFS targeting per platform: -14 Spotify, -16 Apple)
- [ ] Build limiter/maximizer with mode-specific character
- [ ] Implement format-specific export (streaming, vinyl, CD)
- [ ] Integrate A/B preview against commercial references

---

## SPEC-02: Creative Mode Architecture

**Priority:** P0 — Core differentiator  
**Dependencies:** SPEC-01 (mixing/mastering engine)

### 2.1 Mode Definition Schema

Each Creative Mode is a structured configuration containing:

```yaml
mode:
  name: "Eddie Signature"
  type: producer  # or "band_style"
  version: 1.0
  
  arrangement:
    energy_curve: [0.3, 0.5, 0.8, 1.0, 0.6, 0.9, 0.4]  # per-section
    preferred_structures: ["verse-chorus-verse-chorus-bridge-chorus"]
    transition_style: "organic"  # vs "hard_cut", "crossfade"
    
  mixing:
    compression_ratio: 3:1
    compression_character: "transparent"
    low_end: "warm"  # frequency emphasis below 200Hz
    high_end: "smooth"  # de-emphasis above 12kHz
    stereo_width: 0.7  # 0-1 scale
    reverb_style: "room"
    
  instrumentation:
    drum_kit: "vintage_ludwig"
    guitar_tone: "clean_to_mild_overdrive"
    bass_approach: "fingerstyle_round"
    
  mastering:
    target_lufs: -12
    limiter_character: "gentle"
```

**Actionable Tasks:**
- [ ] Design mode schema specification (YAML/JSON)
- [ ] Build 6 initial Producer Modes (Eddie Signature, Live Rock, Studio Polished, Vintage Analogue, Modern Commercial, Experimental)
- [ ] Build 4 initial Band Style Modes (Classic British Rock, 90s Alternative, Funk Rock, Indie Folk)
- [ ] Implement mode parameter interpolation (blend between modes)
- [ ] Create mode A/B comparison tooling for calibration
- [ ] Build feedback capture system (producer approve/reject loop)

### 2.2 Session Players (Virtual Musicians)

**Actionable Tasks:**
- [ ] Integrate or build MIDI generation engine (chord-aware)
- [ ] Train/fine-tune models on genre-specific performance datasets
- [ ] Implement humanization layer (timing/velocity variation)
- [ ] Build chord progression analyzer (input → harmonic context)
- [ ] Create per-instrument "player" profiles tied to Creative Modes

---

## SPEC-03: Live Integration & Session Layer

**Priority:** P1 — Differentiator  
**Dependencies:** SPEC-01, SPEC-02

### 3.1 Score Generation

| Requirement | Target |
|---|---|
| Input | AI-generated MIDI + stems |
| Output formats | MusicXML, PDF, MIDI |
| Accuracy | Pitch + rhythm detection via AnthemScore-class models |
| Deliverables | Per-instrument charts, tempo maps, click tracks |

**Actionable Tasks:**
- [ ] Integrate audio-to-MIDI transcription (AnthemScore, Basic Pitch, or equivalent)
- [ ] Build MusicXML export pipeline
- [ ] Implement PDF score rendering (LilyPond or MuseScore backend)
- [ ] Generate click tracks with tempo map sync
- [ ] Create "rehearsal package" bundler (zip with all charts + audio)

### 3.2 SoundBetter Integration

**Actionable Tasks:**
- [ ] Design API integration with SoundBetter marketplace
- [ ] Build stem replacement workflow (swap AI stem → human recording)
- [ ] Implement session file standardization (tempo, key, format specs for musicians)
- [ ] Create musician brief generator (auto-generate performance notes from Creative Mode)
- [ ] Build upload/review pipeline for incoming human recordings

---

## SPEC-04: Consumer Personalization Layer

**Priority:** P1 — Revenue driver  
**Dependencies:** SPEC-01, SPEC-02

### 4.1 Consumer Input Pipeline

**Actionable Tasks:**
- [ ] Build voice note upload + transcription service
- [ ] Implement mood/genre selection UI (guided wizard)
- [ ] Create lyric generation from user story input
- [ ] Build "melody from humming" detector
- [ ] Implement preview/revision workflow (consumer gets 30-second preview before full render)

### 4.2 Consumer Output & Sharing

**Actionable Tasks:**
- [ ] Generate shareable audio player (embeddable link)
- [ ] Implement social sharing integration (Instagram, TikTok, WhatsApp)
- [ ] Build gift packaging (custom artwork + download link)
- [ ] Create upsell flow (add live vocals, add vinyl pressing, etc.)

---

## SPEC-05: Blockchain Royalty Infrastructure

**Priority:** P2 — Long-term infrastructure  
**Dependencies:** SPEC-01 through SPEC-04 operational

### 5.1 Smart Contract System

**Actionable Tasks:**
- [ ] Select blockchain platform (Polygon, Arbitrum, or Solana for low fees)
- [ ] Design royalty split smart contract (configurable percentages per track)
- [ ] Implement stablecoin payment rails (USDC preferred)
- [ ] Build contributor registry (songwriter, producer mode, session musician, platform)
- [ ] Create payout trigger integration with streaming platform APIs

### 5.2 Provenance & Metadata

**Actionable Tasks:**
- [ ] Design on-chain metadata schema (ISRC, ISWC, contributors, timestamps)
- [ ] Implement timestamped proof-of-authorship for user-contributed elements
- [ ] Build metadata sync with distribution platforms (Spotify, Apple, etc.)
- [ ] Create dispute resolution workflow

---

## SPEC-06: Marketplace & Licensing

**Priority:** P2 — Growth layer  
**Dependencies:** SPEC-02 (modes), SPEC-05 (payments)

**Actionable Tasks:**
- [ ] Design Producer Mode Marketplace (upload, preview, purchase flow)
- [ ] Build verified session musician network (onboarding, rating, availability)
- [ ] Implement sync licensing marketplace (search, preview, license, pay)
- [ ] Create "mode authoring" tools for third-party producers

---

## Infrastructure & Platform

**Priority:** P0 — Cross-cutting  

**Actionable Tasks:**
- [ ] Select cloud provider and define compute architecture (GPU inference fleet)
- [ ] Design API gateway and authentication system
- [ ] Build project/session data model (user → projects → tracks → stems → versions)
- [ ] Implement file storage (S3-compatible, CDN for playback)
- [ ] Design real-time collaboration protocol (if multi-user editing planned)
- [ ] Set up CI/CD pipeline
- [ ] Define security model (encryption at rest/transit, access controls)
- [ ] Build admin dashboard for mode management and analytics
