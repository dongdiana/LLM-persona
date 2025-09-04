```mermaid
flowchart LR
  A["Segment Sampling (by gender, age, household size, and income)"] --> B["Simulation Type A: Simple personas <br> → purchase response"]
  B --> C["Bayesian Update: <br> Prior × Likelihood <br> → Posterior"]
  C --> D["Posterior-weighted Segment sampling <br> → sampled_df (1K)"]
  D --> E["Persona Generation with CoT"]
  E --> F{"Mode Split: New product or not?"}
  F --> G1["MC Mode (Existing product group) <br> → General buyer personas"]
  F --> G2["SW Mode (New product)<br>→ Personas with existing products"]
  G1 --> H["Outputs: personas_{keyword}_all.json"]
  G2 --> H
