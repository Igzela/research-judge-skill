# Example: Paper Review

Prompt:

```text
Use the research-judge skill to compare the algorithms in these papers with the current project notes.
Give a conclusion on which algorithm is more suitable for a single-phase 168-250 Vac input, diode rectifier, 22 uF DC-link, 2.2 kW PMSM centrifugal pump.
```

Expected behavior:

- Extract each algorithm’s real assumptions.
- Compare constraints against the project conditions.
- Identify where papers assume unavailable hardware, sensing, or DC-link capacitance.
- Grade confidence by evidence.
- Recommend the most suitable algorithm and the next simulation or bench validation step.
