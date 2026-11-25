# Digital Electronics notes audit

Reviewed against the three uploaded single-page handwritten scans. This audit separates what is visibly in the notes from corrections and added teaching material.

## 1. Digitals 1 CSE II.pdf — 27 September 2026

### Visible coverage
- Analogue and digital signals.
- Combinational and sequential circuits.
- Binary number notation and conversion examples.
- NOT, AND, OR and XOR gates.
- Half-adder definition, truth table, Boolean expressions and XOR/AND circuit.

### Verified
- Half-adder Sum: `S = A XOR B`.
- Half-adder Carry: `C = AB`.
- The four half-adder truth-table rows match these expressions.

### Corrections / improvements
1. **Sequential circuit wording:** use “The output or next state depends on the present input and the present state.” A sequential circuit has memory/state.
2. **Feedback example:** a single AND gate with its output fed back is not a clear general memory example. Use an SR latch or flip-flop block when illustrating stored state.
3. **Analogue/digital comparison:** avoid absolute statements such as “digital always uses less memory” or “digital circuits are always smaller.” Signal storage and circuit size depend on resolution, encoding, sampling and implementation.
4. **Arithmetic vs Boolean OR:** `1 OR 1 = 1`, while binary arithmetic `1 + 1 = 10₂`.

## 2. Digitals 2.pdf — 14 October 2026

### Visible coverage
- Full-adder definition, truth table, equations and construction using two half adders.
- Half subtractor: definition, truth table, Difference/Borrow equations and circuit.
- Full subtractor: truth table, Difference/Borrow equations and construction using two half subtractors.
- Multiplexer definition and 4:1 MUX selection table/output equation.
- DEMUX is mentioned in the topic outline, but its operation is not developed on the scanned page.

### Formula checks
- Full adder: `S = A XOR B XOR Cin`.
- Full-adder carry: `Cout = AB + ACin + BCin = AB + Cin(A XOR B)`.
- Half subtractor: `D = A XOR B`; `Borrow = A'B`.
- Full subtractor: `D = A XOR B XOR Bin`.
- Full-subtractor borrow: `Bout = A'B + A'Bin + BBin = A'B + Bin(A XOR B)'`.
- The truth-table rows agree with these equations.
- 4:1 MUX selection is `00→I0`, `01→I1`, `10→I2`, `11→I3`.

### Correction
The notes use the phrase “universal logic gate” for a MUX. Replace it with:

> A multiplexer is a data selector and can act as a universal function generator because Boolean functions can be implemented using it. NAND and NOR are the universal logic gates.

The MUX is functionally complete in a circuit-design sense, but the standard universal logic gates are NAND and NOR.

## 3. Digitals 3 CSE I.pdf — 25 October 2026

### Visible coverage
- 2:1, 4:1 and 8:1 multiplexers.
- MUX cascading/construction.
- Implementing Boolean functions using 2:1, 4:1 and 8:1 MUXes.
- Full-adder Sum and Carry implementation using two 8:1 MUXes.
- Universal-gate note at the end of the page.

### Checked examples
- A `2ⁿ:1` MUX requires `2ⁿ − 1` two-input MUXes when built as a binary tree.
- Full-adder outputs as minterms:
  - `Sum = Σm(1,2,4,7)`.
  - `Carry = Σm(3,5,6,7)`.
- For the note example `F(A,B,C)=Σm(1,2,4,5)`, using A,B as the 4:1 MUX select inputs gives `I0=C`, `I1=C'`, `I2=1`, `I3=0`.
- These MUX input maps match the relevant truth-table rows.

## 4. Important material not fully taught by the notes

The website adds complete explanations and worked examples for:
- Number-system conversion procedures, including hexadecimal fractions and decimal fractions.
- 2's-complement subtraction, which is directly asked in both uploaded papers.
- Full NAND, NOR and XNOR truth-table rows and NAND-only/NOR-only constructions.
- Boolean identity, null, idempotent, complement, involution, commutative, associative, distributive and absorption laws; De Morgan's theorems.
- DEMUX operation, selection table and equations.
- Encoder and decoder basics and truth tables.
- K-map grouping rules and the exact 2025 K-map example.
- Quine–McCluskey grouping and the exact 2025 minterm example.

These are added explanations, not claims that the handwritten notes contained them.

## 5. Paper-source warnings

- The 2025 paper scan visibly moves from Q4 to Q6/Q7; Q5 is not visible.
- The 2025 NAND-only implementation expression is blurred around the complements/literals. The website explains a representative NAND–NAND method but does not pretend it is the exact unreadable expression.
- No official 2026 syllabus was uploaded. The friend-provided topic list is therefore treated as tentative. OOP items are excluded from Digital Electronics.

## 6. Review boundary

The three source files are handwritten scans. The main headings and most equations/tables are readable; some small labels in diagrams are not. Any such unclear detail is flagged rather than reconstructed as a fact.
