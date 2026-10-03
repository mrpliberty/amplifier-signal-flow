# Signal / Power

An interactive, single-page field guide to amplifier signal flow. Choose a topology, follow its audio and power paths, inspect each stage, step through four signal moments, or play an automatic trace. The output study illustrates crossover, PWM, and rail headroom.

## Run locally

No build step or dependencies are required. Open `index.html` in a browser, or run a local server:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000. Fonts are optionally fetched from Google Fonts; system fallbacks work offline. The app itself is plain HTML, CSS and JavaScript.

## Publish on GitHub Pages

Push these four files to the repository root, then in **Settings → Pages** choose **Deploy from a branch**, branch `main`, folder `/ (root)`. GitHub Pages serves `index.html` at the URL shown there; no build or configuration is required.

## The six views

1. **Low-power SET / Class A:** one continuously conducting power triode, conventional single-ended transformer, idle dissipation.
2. **Class B:** complementary output devices alternate half-cycles, with an illustrative non-prebiased BJT crossover notch.
3. **Class AB:** a bias spreader creates small conduction overlap near zero and smooths the handoff.
4. **Class D:** analog-input PWM modulation, switching H-bridge, illustrative optional LC output filter and differential speaker connection.
5. **Class G & H:** discrete rail selection versus envelope tracking, shown as power-supply overlays on an AB audio output stage.
6. **Push-Pull vs Single-Ended:** representative tube circuits contrast one continuously conducting output tube with a phase-split pair and center-tapped transformer. Output architecture is independent of operating class.

Orange arrows represent the audio path; blue dashed arrows are DC power; teal dashed arrows indicate feedback; red dotted arrows indicate control. The supply provides speaker energy — the input only controls it.

These conceptual diagrams are **not buildable schematics**. Details vary by implementation; tube B+ voltages can be lethal. Class D filterless designs exist; Class G/H naming and rail implementation vary. The push-pull comparison specifically uses tube examples, not all transistor push-pull circuits.

## References

- [The Valve Wizard — Single Ended Output Stage](https://www.valvewizard.co.uk/se.html)
- [The Valve Wizard — Push-Pull Power Output Stage](https://www.valvewizard.co.uk/pp.html)
- [Analog Devices — Class B and AB amplifiers](https://wiki.analog.com/university/courses/engineering_discovery/lab_14)
- [Texas Instruments — Class-D LC Filter Design](https://www.ti.com/jp/lit/an/sloa119b/sloa119b.pdf)
- [Texas Instruments — Benefits of Class-G and Class-H Boost](https://www.ti.com/lit/pdf/slaa888)

Copyright © 2026. Educational illustration; not an electronics construction guide.
