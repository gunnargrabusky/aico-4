# AICO-4
### Artificial Intelligence Communication Ontology

A symbolic protocol for AI-to-AI communication, designed for token-efficient agent orchestration. AICO-4 replaces verbose natural language instructions between agents with a dense, typed, formally complete symbolic grammar.

**17–53% token reduction over natural language equivalents** — the more complex the instruction, the greater the savings.

---

## What is AICO-4?

When AI agents communicate with each other — passing instructions, routing tasks, validating outputs, coordinating pipelines — they typically do so in natural language or JSON. Both are expensive. Natural language is verbose by design. JSON is structured but untypes semantics, leaving meaning implicit.

AICO-4 is a symbolic grammar purpose-built for AI-to-AI transmission. Every token carries typed, unambiguous meaning. A 170-token natural language instruction becomes a 60–80 token AICO-4 transmission with no loss of precision — and in testing, often with *more* architectural clarity in the output.

```
⟪OPEN⟫ · ∇[v:4.0] · ∇CAP{MACRO · SESSION · VALIDATE}

⟨AI:ALPHA⟩ → ⟨AI:BETA⟩
λ:WRITE[⟦LANG=𝕊:"TypeScript"⟧ · ⟦QUAL=Φ⁴⟧ · ⟦DEPTH=Δ+⟧]
· ⇒✓{𝔹:TYPED · 𝔹:DOCS · ✓[∄ ERR]} ⇒ 𝕊:MODULE
```

---

## Core Values

`semantic density` · `zero ambiguity` · `positional grammar` · `zero filler`
`typed safety` · `pipeline integrity` · `formal completeness`

---

## Token Reduction — Test Results

Three prompt variants for the same task were measured using Gemini's native Tokenizer API:

| Prompt type | Tokens | Reduction |
|---|---|---|
| Natural language | ~170 | baseline |
| AICO-4 base | ~80 | ~53% |

Reduction scales with instruction complexity. Simple single-hop queries compress modestly (17%). Complex multi-parameter orchestration instructions with typed contracts and pipeline routing compress maximally (53–65%).

---

## Spec Contents

The full specification (`AICO-4_full_key.txt`) covers 33 sections:

| Sections | Contents |
|---|---|
| 1–18 | Token vocabulary — glyphs, operators, types, modifiers, tense, confidence, attribution |
| 19–25 | Structural layers — session, macros, type inference, error contracts, memory, topology |
| 26–29 | Quality contracts, grammar rules, example transmissions, expressive capabilities |
| 30–33 | Extended layers — arithmetic, pipelines, broadcast, ∇PECS parser configuration |

---

## Quick Reference

**Entities**
```
⟨AI⟩    AI agent        ⟨H⟩     Human
⟨SYS⟩   System          ⟨∅⟩     Null / void
```

**Operators**
```
→    Directed send       ↔    Bidirectional exchange
↠    Pipeline feed       ⇝    Broadcast (one to many)
⊕    Peer link           ⊗    Fork
⊙    Join                ⊩    Derives
```

**Types**
```
𝕊    String      𝕀    Integer     𝔽    Float
𝔹    Boolean     𝕃    List        𝕄    Map
𝕋    Infer       𝔻    Dynamic     𝕍    Void
```

**Quality tiers**
```
Φ¹   Prototype    Φ²   Draft    Φ³   Clean    Φ⁴   Production
```

**Confidence**
```
κ¹   Certain    κ²   High    κ³   Medium    κ⁴   Low    κ⊘   Unknown
```

**Validation contracts**
```
⇒✓{𝔹:TYPED · 𝔹:DOCS · ✓[∄ ERR]}    Output must be typed, documented, error-free
⊞✓{✓[κ¹]}                            Input must be verified/certain
✗{𝕊:PATTERN}                         Output must not contain pattern
```

**Session control**
```
⟪OPEN⟫          Open session
⟪CLOSE⟫         Close session
∇[v:4.0]        Declare AICO-4.0 compliance
∇CAP{...}       Declare supported feature flags
ACK / NAK[n]    Acknowledge / reject with reason code
```

---

## Example Transmission

A multi-agent pipeline: plan → write → test → review

```
⟪OPEN⟫ · ∇[v:4.0] · ∇CAP{MACRO · SESSION · VALIDATE · STREAM}

⟨AI:PLANNER⟩ ↠ ⟨AI:CODER⟩ ↠ ⟨AI:TESTER⟩ ↠ ⟨AI:REVIEWER⟩

⊗ ⌈
  ⟨AI:TESTER⟩   ↠ λ:TEST[𝕃𝔾:"TypeScript" · 𝕋𝔽:"Jest"] · ⇒ 𝕄[𝕊:𝔻]:JSON
  ⟨AI:REVIEWER⟩ ↠ λ:REVIEW[Φ⁴ · 𝔾[*]]                 · ⇒ 𝕊:REPORT
⌉

⊙[∀] · ⇒✓{𝔹:TYPED · ✓[∄ ERR]} ⇒ 𝕃[𝕊]:FILES
```

---

## Contributing

The spec is open. If you find ambiguities, propose token additions, or test against models not yet benchmarked — open an issue or PR.

---

## Citation

If you use AICO-4 in research or build on it, please cite:

```
Grabusky, G. (2025). AICO-4: Artificial Intelligence Communication Ontology.
https://github.com/gunnargrabusky/aico-4
```

---

## License

CC0-1.0 — public domain. Use it, build on it, implement it, no restrictions.
