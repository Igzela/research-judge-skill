# Example: Technical Decision

Prompt:

```text
Use the research-judge skill to review this power supply design direction.
Focus on 30V startup reliability, thermal risk at high input voltage, transformer assumptions, and what must be validated before mass production.
```

Expected behavior:

- Treat measured test results as stronger than theoretical guesses.
- Separate calculation, assumption, and empirical evidence.
- Scan from architect, reliability engineer, cost owner, manufacturing, testing, and skeptic perspectives.
- Identify failure assumptions.
- Recommend validation tests before locking the design.
