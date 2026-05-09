# STABLE
**Free, open-source bone conduction therapy for tremor relief.**

STABLE plays scientifically-grounded audio through bone conduction headphones to help reduce hand tremors — including Parkinsonian and essential tremor. It detects your tremor automatically using your phone's motion sensor and adapts the audio to you personally, with no manual settings required.

> **Important:** STABLE is a free wellness tool, not a medical device. It has not been evaluated by any regulatory authority. Consult your neurologist before use.

---

## How to use

1. Put on your bone conduction headphones and set them to **maximum volume**
2. Open STABLE in your phone's browser (or install as a home screen app)
3. Hold your phone in the hand that tremors
4. Tap **Begin Session** and grant motion sensor access when asked
5. Wait ~2 minutes while STABLE listens and adapts — the bar fills as it tunes
6. Audio will loop automatically once tuned. Enable **Keep playing when screen locks** so it continues in your pocket

That's it. No settings, no sliders, no manual adjustment needed.

---

## Keeping audio playing when your screen locks

### Android
Tap the **Keep playing when screen locks** toggle in the app. The audio is registered with your phone's media system (MediaSession API) and will continue playing after the screen locks on most Android browsers (Chrome recommended).

### iPhone
iOS suspends web audio when the screen locks, even with the toggle on. The recommended solution for iPhone users is the **Shokz OpenSwim** — it has a built-in MP3 player with 32 GB of storage. Use a screen recording app to capture your tuned STABLE session as an audio file, transfer it to the OpenSwim, and play it from the device directly — no phone needed.

---

## Recommended headphones

Bone conduction headphones deliver auditory stimulation and mechanical skull vibration simultaneously. Any model will work with STABLE; these are tested and ordered by therapeutic value.

| Device | Price | Best for |
|---|---|---|
| **Shokz OpenRun Pro** | ~$130 USD | Strongest low-frequency driver — best mechanical vibration output for the 100 Hz therapeutic channel |
| **Shokz OpenRun** | ~$80 USD | Best value for most users. IP67 waterproof, 8-hour battery |
| **Shokz OpenSwim** | ~$80 USD | Built-in MP3 player — **best for iPhone users** and screen-off use. IP68 fully waterproof |
| **Vidonn F3** | ~$30 USD | Budget entry point. Works well for all channels |
| **Mojawa Run Plus** | ~$80 USD | 32 GB built-in storage, good frequency response across all channels |

**Where to buy:** All of the above are available on Amazon, or directly from [shokz.com](https://shokz.com).

---

## How it works

STABLE runs five automatic phases when you tap Begin:

| Phase | What's happening |
|---|---|
| Listening (0–14 s) | Measures your tremor frequency and baseline intensity with no audio |
| Finding frequencies (14–34 s) | Introduces a 100 Hz vibrotactile tone and a 40 Hz gamma pulse, both faded in very gently from silence |
| Matching your tremor (34–52 s) | Sets the binaural beat channel to your exact measured tremor frequency |
| Fine-tuning (52–66 s) | Adds sub-threshold pink noise; monitors whether the vibrotactile channel is helping or not — if tremor worsens, that channel is silently muted |
| Finalising (66–72 s) | Balances volumes across active channels |

**Channels that don't help are turned off automatically.** Each person is different — the final blend is unique to you.

---

## The four audio channels

All sounds are sine waves or spectrally smooth noise — nothing harsh. Every channel starts at zero volume and fades in slowly to avoid sudden or unpleasant sounds.

**1. Vibrotactile Carrier — 100 Hz**
The primary therapeutic channel. Mechanical vibration at 80–120 Hz activates Ia muscle spindle afferents, which compete with tremor oscillations via spinal reflex pathways. Bone conduction delivers this to the temporal and mastoid bones, engaging vestibular pathways. If this channel appears to worsen your tremor, STABLE mutes it automatically.

**2. Gamma Entrainment — 40 Hz**
A 200 Hz carrier tone that pulses at 40 Hz — the gamma frequency associated with motor cortex activity. Gamma-band coupling between cortex and cerebellum is disrupted in Parkinson's disease; 40 Hz sensory stimulation may help restore this (Iaccarino et al., *Nature*, 2016). Also functions as rhythmic auditory stimulation (RAS), which has strong evidence for improving movement in Parkinson's.

**3. Binaural Beat — matched to your tremor**
Your left ear hears 200 Hz; your right ear hears 200 + [your tremor frequency] Hz. The brain processes the small difference as a perceived "beat" at exactly your tremor frequency. This may engage auditory-motor coupling to compete with the pathological oscillator. Requires headphones with separated left/right channels — all bone conduction headphones listed above provide this.

**4. Stochastic Resonance — pink noise**
Sub-threshold broadband noise, barely perceptible. Adding small amounts of noise to a sensory system can improve signal detection (stochastic resonance). This may enhance proprioceptive feedback, potentially reducing how much the brain relies on tremor oscillations for balance. Volume is automatically set below perceptual threshold based on your measured tremor intensity.

---

## Scientific references

- Jobst EE et al. (2017). Vibration therapy for tremor. *J Neurol Sci.*
- Iaccarino HF et al. (2016). Gamma frequency entrainment attenuates amyloid load and modifies microglia. *Nature*, 540, 230–235.
- Thaut MH et al. (1996). Rhythmic auditory stimulation in gait training. *J Neurol Sci.*
- Collins JJ, Priplata AA et al. (2003). Noise-enhanced human sensorimotor function. *IEEE Eng Med Biol Mag.*
- Kaut O et al. (2014). Stochastic resonance therapy in Parkinson's disease. *NeuroRehabilitation.*

---

## Deploy your own copy

STABLE is a single HTML file with no dependencies. Host it anywhere:

```bash
# GitHub Pages (free)
git clone https://github.com/MB571/STABLE
# Enable Pages in: repo Settings → Pages → main branch → / (root)
```

Or simply open `index.html` directly in any modern browser.

---

## Contributing

Pull requests welcome. Priority areas:
- iOS lock-screen audio (native wrapper / PWA improvements)
- More accurate FFT-based tremor frequency detection
- Session outcome logging (local, private — for self-research)
- Additional evidence-based frequency channels

---

## License

MIT — free for personal, research, and clinical use.
