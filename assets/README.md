# Inceptron brand guide

<p align="center">
  <img src="palette.svg" alt="The Inceptron palette: aquamarine, sapphire, fuchsia and ruby glass on a deep tan ground, shown on an OKLCH hue wheel" width="100%">
</p>

## The mark

Three panes of tinted glass (aquamarine, sapphire and fuchsia), each turned 12° further than the last, hold a **ruby-glass ∎**, the symbol that ends a proof. It is a picture of how proofs work: every proof is built from smaller proofs, all the way down to the kernel, and every one of them ends in ∎.

## The four gems

Each colour has one job.

| Gem | Hex | OKLCH | Role |
| --- | --- | --- | --- |
| **Aquamarine** | `#2FDAC4` | `oklch(0.80 0.135 182)` | Light. The outer pane, the turnstile ⊢, tactic names. |
| **Sapphire** | `#073FE3` | `oklch(0.47 0.25 264)` | Stones and depth. The middle pane and the cut sapphires. |
| **Fuchsia** | `#DA02AF` | `oklch(0.60 0.26 340)` | Energy. The inner pane and keywords. |
| **Ruby** | `#C30839` | `oklch(0.52 0.205 18)` | Glass. The ∎ that closes every proof. |

Each gem also has a light tint (highlights, and text on tan) and a deep shade (glass edges and tinted shadows), all at the same hue.

## The ground

| Name | Hex | Use |
| --- | --- | --- |
| Tan light | `#9B794F` | Where the light falls, top left |
| Deep tan | `#7F5B32` | The main ground |
| Tan deep | `#664524` | Panels and the proof card |
| Umber | `#422A16` | Pills, badge labels and shadows |
| Ivory | `#FEF6E7` | Wordmark and primary text |
| Sand | `#F0DFC4` | Secondary text |

## Colour theory

**A warm ground for cool jewels.** Deep tan is a low-chroma orange, at about 68° on the OKLCH hue wheel. Sapphire sits almost directly opposite at 264°, so the stones and the middle pane carry the strongest contrast. Aquamarine sits on the same cool side of the wheel, so it contrasts with the tan too. Ruby and fuchsia are the tan's warm neighbours and sit in harmony with it. The result is one quiet neutral and four saturated accents.

**Saturation at the limit, in small doses.** Each gem's chroma is pushed close to the most a screen can show at its lightness (sapphire 0.25, fuchsia 0.26). That is why they read as jewels rather than paint. The restraint comes from area instead: roughly 70% of any piece is tan, 25% is glass and stone, and 5% is ruby.

**Why tan, not black.** You see glass through what it does to the surface behind and beneath it: it tints it, bends it, and casts a coloured shadow on it. On black there is nothing to tint, so glass can only glow. A mid-dark, warm ground lets the panes be see-through and their shadows take on colour. It also keeps contrast softer than neon on black, which makes the whole thing calmer.

**How the glass is drawn.** Seen from above, real glass is most saturated at its rim, where light passes through the most material, and nearly clear in the middle. Each pane has:

- a saturated, bevelled rim, lighter where it faces the light and deeper where it turns away
- a nearly clear face with a faint sheen
- a bright specular edge at the top left
- a coloured rim light at the bottom right, where light leaves the glass
- a shadow tinted with the pane's own colour

The ruby is cut with a lighter table facet, and the sapphires are brilliant-cut, with each facet shaded by its angle to the light. Everything is lit from the top left.

**Gradients go the long way round.** Blending two near-complements directly in sRGB passes through grey: the midpoint of aquamarine and ruby is a muddy `#79717E`. The signature gradient instead travels round the wheel through sapphire and fuchsia. It is interpolated in OKLCH with 13 stops, so it stays vivid the whole way. The bottom of the palette sheet shows both versions side by side.

**Perceptual lightness.** OKLCH lightness matches how bright colours actually look. So each gem's tint and shade are made by moving lightness alone, with the hue fixed, and each family stays recognisable from its palest tint to its deepest shade.

## Contrast

Measured with the WCAG contrast formula.

On deep tan `#7F5B32`, used for the wordmark and tagline:

| Colour | Ratio | WCAG |
| --- | --- | --- |
| Ivory | 5.7 : 1 | AA (AAA for large text) |
| Sand | 4.7 : 1 | AA |

On tan deep `#664524`, used for code on the proof card:

| Colour | Ratio | WCAG |
| --- | --- | --- |
| Ivory | 8.0 : 1 | AAA |
| Aqua light `#B4F8EB` | 7.2 : 1 | AAA |
| Fuchsia light `#FEB8E6` | 5.4 : 1 | AA |
| Ruby light `#FDB4BA` | 5.1 : 1 | AA |
| Sapphire light `#96C0FE` | 4.6 : 1 | AA |

Base gem colours are for glass, stones and shapes, not small text. The README badges put white text on the gems: sapphire 7.4 : 1, ruby 6.2 : 1 and fuchsia 4.6 : 1. Aquamarine is too light for white text, so its badge uses deep aqua `#08837A` (4.6 : 1).

## Typography

- **Wordmark:** Inter Display Bold, tracking −1.8%, in ivory with a soft umber shadow
- **Text:** Inter Medium and SemiBold
- **Code and maths:** JetBrains Mono Medium

All text in the artwork is converted to outlines, so it looks identical on every device. Both typefaces are released under the SIL Open Font License.

## Files

| File | Use |
| --- | --- |
| `banner.svg` | README header. The gems sparkle gently; the animation stops for viewers who have asked their system for reduced motion. |
| `logo.svg` | Square logo and avatar |
| `social-preview.jpg` | Link preview image (1280 × 640). Upload it in **Settings → General → Social preview**. |
| `social-preview.svg` | Source for the JPEG |
| `proof-card.svg` | The proof illustration in the README |
| `icons/*.svg` | Feature icons, one gem each |
| `divider.svg` | Section divider |
| `palette.svg` | The palette sheet at the top of this page |
