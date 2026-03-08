# IRREVOCULL

Primitive ID: PRIM-007  
Package: @verifrax/irrevocull  
Binary: irrevocull

Verifrax primitive — judgment primitive for deterministic irreversible systems.

---

## Status

Current release status: pre-stable primitive release line.

Canonical release target:

package version: 0.1.0  
tag: v0.1.0

IRREVOCULL is part of the Verifrax primitive layer and follows the canonical primitive governance, naming, version, and packaging rules.

---

## Purpose

IRREVOCULL renders judgment over an already-fixed verification and attestation state.

Once origin is established, custody is preserved, time is fixed, boundaries are enforced, verification is completed, and attestation has witnessed the result, the system still needs a judgment primitive that can issue a deterministic decision. IRREVOCULL exists to perform that role.

It does not establish origin. It does not preserve custody. It does not set time boundaries. It does not enforce system boundaries. It does not perform primary verification. It does not create the witness layer. It does not terminate lifecycle. Its role is narrower: issue judgment from already-established prior state.

---

## What This Primitive Does

- renders deterministic judgment from prior verified and attested state
- transforms verified evidence into a judgment outcome
- produces decision output suitable for final downstream termination or enforcement

---

## What This Primitive Does Not Do

- does not establish first origin
- does not preserve custody continuity
- does not fix temporal ordering
- does not enforce operational boundaries
- does not perform primary verification itself
- does not create attestation witness state
- does not terminate lifecycle

---

## Behavioral Contract

Invocation model:

executable: irrevocull  
package: @verifrax/irrevocull  
runtime: CLI-first

The primitive operates only after origin, custody, time, boundary, verification, and attestation have already been completed.

If no stable attested verification state exists, IRREVOCULL must not fabricate a judgment.

Exit codes:

0 — judgment completed successfully  
non-zero — invocation failed or contract violated

---

## Usage

Install:

npm install -g @verifrax/irrevocull

Execute:

irrevocull artifact.json

stdin example:

cat artifact.json | irrevocull

---

## Determinism Guarantees

For identical canonical input, IRREVOCULL must produce identical judgment output.

No hidden environmental state may influence the result.

IRREVOCULL assumes prior primitives have already constrained origin, custody, time, boundary, verification, and attestation. It does not substitute for any earlier primitive and does not replace final termination.

---

## Security Model

IRREVOCULL protects against ambiguity in final decision state.

Its security value is to ensure that a decision is rendered from already-determined evidence under deterministic judgment rules. It does not establish proof surfaces upstream and does not itself terminate lifecycle state.

---

## Relationship to Other Primitives

Canonical primitive order:

1 originseal  
2 archicustos  
3 kairoclasp  
4 limenward  
5 validexor  
6 attestorium  
7 irrevocull  
8 guillotine

Repositories:

https://github.com/Verifrax/originseal  
https://github.com/Verifrax/archicustos  
https://github.com/Verifrax/kairoclasp  
https://github.com/Verifrax/limenward  
https://github.com/Verifrax/validexor  
https://github.com/Verifrax/attestorium  
https://github.com/Verifrax/irrevocull  
https://github.com/Verifrax/guillotine

---

## Installation

npm install -g @verifrax/irrevocull

command -v irrevocull

Repository:
- GitHub: https://github.com/Verifrax/irrevocull
- Package: @verifrax/irrevocull
- Binary: irrevocull

---

## License

MIT
