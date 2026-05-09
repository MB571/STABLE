# STABLE *Signals Tuned for Assistive Bone-Level Equilibration*

**Free, open-source bone conduction therapy for tremor relief.**

**[Open the app on your phone](https://mb571.github.io/STABLE/)**

STABLE plays scientifically-grounded audio through bone conduction headphones to help reduce hand tremors, including Parkinsonian and essential tremor. It detects your tremor automatically using your phone's motion sensor and adapts the audio to you personally, with no manual settings required.

> **Important:** STABLE is a free wellness tool, not a medical device. It has not been evaluated by any regulatory authority. Consult your neurologist before use.

---

## How to use

1. Put on your bone conduction headphones and set them to **maximum volume**
2. Open STABLE in your phone's browser (or install as a home screen app)
3. Hold your phone in the hand that tremors
4. Tap **Begin Session** and grant motion sensor access when asked
5. Wait ~2 minutes while STABLE listens and adapts; the bar fills as it tunes
6. Audio will loop automatically once tuned. Enable **Keep playing when screen locks** so it continues in your pocket

That's it. No settings, no sliders, no manual adjustment needed.

---

## Keeping audio playing when your screen locks

### Android
Tap the **Keep playing when screen locks** toggle in the app. The audio is registered with your phone's media system (MediaSession API) and will continue playing after the screen locks on most Android browsers (Chrome recommended).

### iPhone
iOS suspends web audio when the screen locks, even with the toggle on. The recommended solution for iPhone users is the **Shokz OpenSwim**: it has a built-in MP3 player with 32 GB of storage. Use a screen recording app to capture your tuned STABLE session as an audio file, transfer it to the OpenSwim, and play it from the device directly. No phone needed.

---

## Recommended headphones

Bone conduction headphones deliver auditory stimulation and mechanical skull vibration simultaneously. Any model will work with STABLE; these are tested and ordered by therapeutic value. I have no affilliations with any brands these were some initial searches that matched my frequencies used.

| Device | Price | Best for |
|---|---|---|
| **Shokz OpenRun Pro** | ~$130 USD | Strongest low-frequency driver, best mechanical vibration output for the 100 Hz therapeutic channel |
| **Shokz OpenRun** | ~$80 USD | Best value for most users. IP67 waterproof, 8-hour battery |
| **Shokz OpenSwim** | ~$80 USD | Built-in MP3 player, best for iPhone users and screen-off use. IP68 fully waterproof |
| **Vidonn F3** | ~$30 USD | Budget entry point. Works well for all channels |
| **Mojawa Run Plus** | ~$80 USD | 32 GB built-in storage, good frequency response across all channels |

**Where to buy:** All of the above are available on Amazon, or directly from [shokz.com](https://shokz.com).

---

## How it works

STABLE runs six automatic phases when you tap Begin:

| Phase | What's happening |
|---|---|
| Listening (0-14 s) | Measures your tremor frequency and baseline intensity with no audio |
| Testing 100 Hz (14-33 s) | Introduces vibrotactile tone, faded in from silence; measures whether tremor reduces |
| Testing 40 Hz (33-54 s) | Introduces gamma pulse, same process |
| Binaural beat (54-72 s) | Sets beat frequency to your exact measured tremor frequency and tests it |
| Stochastic noise (72-86 s) | Adds sub-threshold pink noise and monitors for any adverse response |
| Finalising (86-100%) | Balances volumes across all channels that proved helpful |

**Channels that don't help are turned off automatically.** Each person responds differently; the final blend is unique to you.

---

## The four audio channels

All sounds are sine waves or spectrally smooth noise (nothing harsh). Every channel starts at zero volume and fades in slowly to avoid sudden or unpleasant sounds.

**1. Vibrotactile Carrier (100 Hz)**
The primary therapeutic channel. Mechanical vibration at 80-120 Hz activates Ia muscle spindle afferents, which compete with tremor oscillations via spinal reflex pathways. Bone conduction delivers this to the temporal and mastoid bones, engaging vestibular pathways. If this channel appears to worsen your tremor, STABLE mutes it automatically.

**2. Gamma Entrainment (40 Hz)**
A 200 Hz carrier tone that pulses at 40 Hz, the gamma frequency associated with motor cortex activity. Gamma oscillations in the basal ganglia-thalamo-cortical circuit are pathologically reduced in Parkinson's disease; restoring them via 40 Hz entrainment has been shown to recover primary motor cortex plasticity in PD patients (Guerra et al., *Journal of Neuroscience*, 2020). Also functions as rhythmic auditory stimulation (RAS), which has direct evidence for improving movement in Parkinson's (Thaut et al., 1996).

**3. Binaural Beat (matched to your tremor)**
Your left ear hears 200 Hz; your right ear hears 200 + [your tremor frequency] Hz. The brain processes the small difference as a perceived "beat" at exactly your tremor frequency. This may engage auditory-motor coupling to compete with the pathological oscillator. Requires headphones with separated left/right channels; all bone conduction headphones listed above provide this.

**4. Stochastic Resonance (pink noise)**
Sub-threshold broadband noise, barely perceptible. Adding small amounts of noise to a sensory system can improve signal detection (stochastic resonance). This may enhance proprioceptive feedback, potentially reducing how much the brain relies on tremor oscillations for balance. Volume is automatically set below perceptual threshold based on your measured tremor intensity.

---

## Scientific references

**Vibrotactile stimulation and tremor**
- Jobges EM et al. (2002). Vibratory proprioceptive stimulation affects Parkinsonian tremor. *Parkinsonism and Related Disorders*, 8(3), 171-176. [doi:10.1016/s1353-8020(01)00016-5](https://doi.org/10.1016/s1353-8020(01)00016-5)
- Tabacof L et al. (2021). Safety and Tolerability of a Wearable, Vibrotactile Stimulation Device for Parkinson's Disease. *Frontiers in Human Neuroscience*, 15, 712621. [doi:10.3389/fnhum.2021.712621](https://doi.org/10.3389/fnhum.2021.712621)
- Cabral AM et al. (2024). On the Effect of Vibrotactile Stimulation in Essential Tremor. *Healthcare*, 12(4), 448. [doi:10.3390/healthcare12040448](https://doi.org/10.3390/healthcare12040448)

**Gamma entrainment (40 Hz)**
- Guerra A et al. (2020). Enhancing Gamma Oscillations Restores Primary Motor Cortex Plasticity in Parkinson's Disease. *Journal of Neuroscience*, 40(24), 4788-4796. [doi:10.1523/JNEUROSCI.0357-20.2020](https://doi.org/10.1523/JNEUROSCI.0357-20.2020)
- Iaccarino HF et al. (2016). Gamma frequency entrainment attenuates amyloid load and modifies microglia. *Nature*, 540, 230-235. (40 Hz sensory entrainment produces measurable neurological change; original work is in an Alzheimer's mouse model.) [doi:10.1038/nature20587](https://doi.org/10.1038/nature20587)

**Rhythmic auditory stimulation**
- Thaut MH et al. (1996). Rhythmic auditory stimulation in gait training for Parkinson's disease patients. *Movement Disorders*, 11(2), 193-200. [doi:10.1002/mds.870110213](https://doi.org/10.1002/mds.870110213)

**Binaural beats**
- Calvano A et al. (2023). Binaural acoustic stimulation in patients with Parkinson's disease. *Frontiers in Neurology*, 14, 1167006. [doi:10.3389/fneur.2023.1167006](https://doi.org/10.3389/fneur.2023.1167006)
- Jirakittayakorn N & Wongsawat Y (2017). Brain Responses to a 6-Hz Binaural Beat: Effects on General Theta Rhythm and Frontal Midline Theta Activity. *Frontiers in Neuroscience*, 11, 365. [doi:10.3389/fnins.2017.00365](https://doi.org/10.3389/fnins.2017.00365)

**Stochastic resonance**
- Collins JJ, Priplata AA et al. (2003). Noise-enhanced human sensorimotor function. *IEEE Eng Med Biol Mag*, 22(2), 76-83. [doi:10.1109/MEMB.2003.1195700](https://doi.org/10.1109/MEMB.2003.1195700)
- Kaut O et al. (2011). Stochastic resonance therapy in Parkinson's disease. *NeuroRehabilitation*, 28(4), 353-358. [doi:10.3233/NRE-2011-0663](https://doi.org/10.3233/NRE-2011-0663)
- Kaut O et al. (2016). Postural Stability in Parkinson's Disease Patients Is Improved after Stochastic Resonance Therapy. *Parkinson's Disease*, 2016, 7948721. [doi:10.1155/2016/7948721](https://doi.org/10.1155/2016/7948721)

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
- Session outcome logging (local, private, for self-research)
- Additional evidence-based frequency channels

---

## License

MIT License. Free for personal, research, and clinical use.
