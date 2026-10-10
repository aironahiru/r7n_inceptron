<p align="center">
  <img src="assets/banner.svg" alt="Inceptron, a new theorem prover for advanced arithmetic" width="100%">
</p>

<p align="center">
  <a href="LICENSE"><img alt="License: Apache 2.0" src="https://img.shields.io/badge/license-Apache_2.0-073FE3?style=flat-square&labelColor=422A16"></a>
  <img alt="Status: early development" src="https://img.shields.io/badge/status-early_development-DA02AF?style=flat-square&labelColor=422A16">
  <a href="CONTRIBUTING.md"><img alt="PRs welcome" src="https://img.shields.io/badge/PRs-welcome-08837A?style=flat-square&labelColor=422A16"></a>
  <a href="CODE_OF_CONDUCT.md"><img alt="Contributor Covenant 2.1" src="https://img.shields.io/badge/Contributor_Covenant-2.1-C30839?style=flat-square&labelColor=422A16"></a>
</p>

<p align="center">
  <b>Prove things about numbers: rigorously, readably, and with a little help from the machine.</b>
</p>

<p align="center">
  <a href="#why-inceptron">Why Inceptron?</a> &nbsp;·&nbsp;
  <a href="#a-taste-of-inceptron">A taste</a> &nbsp;·&nbsp;
  <a href="#roadmap">Roadmap</a> &nbsp;·&nbsp;
  <a href="#get-involved">Get involved</a>
</p>

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

## Welcome

**Inceptron** is a new theorem prover built for **advanced arithmetic**: the natural numbers, the integers, the rationals, and everything you can say about them, from divisibility and congruences to inequalities and induction.

The goal is simple to state and fun to chase: when you know *why* a statement about numbers is true, writing a machine-checked proof of it should feel as natural as explaining it on a whiteboard.

> [!NOTE]
> Inceptron is brand new. There is no code to run yet, and the design is happening in the open. This is the best time to share ideas and help shape what it becomes.

## Why Inceptron?

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><img src="assets/icons/arithmetic.svg" alt="" width="48"><br>Arithmetic first</h3>
      Numbers are the main focus, not one library among many. ℕ, ℤ, ℚ, divisibility, modular arithmetic and inequalities are built in.
    </td>
    <td width="50%" valign="top">
      <h3><img src="assets/icons/core.svg" alt="" width="48"><br>Small, trusted core</h3>
      A minimal kernel checks every proof, so the amount of code you have to trust stays small.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><img src="assets/icons/automation.svg" alt="" width="48"><br>Automation that shows its work</h3>
      Decision procedures handle the tedious steps, and each one produces a proof the kernel can check.
    </td>
    <td width="50%" valign="top">
      <h3><img src="assets/icons/readable.svg" alt="" width="48"><br>Proofs you can read</h3>
      Proof scripts should read like the argument a mathematician would give.
    </td>
  </tr>
</table>

## A taste of Inceptron

<p align="center">
  <img src="assets/proof-card.svg" alt="An illustrative Inceptron proof that 6 divides n³ − n for every integer n" width="100%">
</p>

> [!IMPORTANT]
> This is an illustration of the direction, not working code. The syntax is still being designed.

Three consecutive integers always include a multiple of 2 and a multiple of 3, so 6 divides their product. Each `by` step hands a small, well-defined job to the machine, and you can read the whole argument from top to bottom.

<details>
<summary>Show the proof as plain text</summary>

```text
theorem six_divides : ∀ n : ℤ,  6 ∣ n³ − n

proof
  have n³ − n = (n − 1) · n · (n + 1)      by ring
  have 2 ∣ (n − 1) · n · (n + 1)           by cases n mod 2
  have 3 ∣ (n − 1) · n · (n + 1)           by cases n mod 3
  conclude 6 ∣ n³ − n                      by coprime 2 3
∎
```

</details>

## Roadmap

A first sketch. It will change as the design takes shape, and suggestions are welcome.

- [x] Set up the repository and community guidelines
- [ ] Design document: logic, kernel and proof format
- [ ] Minimal proof-checking kernel
- [ ] Parser and pretty-printer for the proof language
- [ ] Core arithmetic library: ℕ, ℤ, ℚ, divisibility, congruences
- [ ] Decision procedures for linear arithmetic and modular reasoning
- [ ] Interactive mode and editor support
- [ ] Documentation site with tutorials and worked examples

## Getting started

There's nothing to install yet. To follow along:

- **Star** the repository to bookmark it.
- **Watch → Custom → Releases** to hear about the first release.

## Get involved

Inceptron is just getting started, so contributions now have an outsized effect. You don't need to be an expert in logic to help:

- **Share an idea**, or a theorem you'd love to prove, by [opening an issue](https://github.com/aironahiru/r7n_inceptron/issues/new/choose).
- **Point us to prior art**: papers, tools and techniques we should learn from.
- **Report problems** as soon as there is something to break.
- **Contribute changes**: the [contributing guide](CONTRIBUTING.md) explains how.

Everyone taking part is expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## License

Inceptron is released under the [Apache License 2.0](LICENSE).

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<p align="center">
  <img src="assets/logo.svg" alt="" width="64"><br>
  <sub>Made with ∎ by <a href="https://github.com/aironahiru">@aironahiru</a> and contributors · <a href="assets/README.md">Brand &amp; palette</a></sub>
</p>
