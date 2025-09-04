```mermaid
flowchart LR
  A["Segment Sampling: 1,000 simple personas"] --> B["1st Simulation Type A - 1,000 simple personas"]
  B --> C["Bayesian Update: Prior × Likelihood → Posterior"]
  C --> D["Posterior-weighted Sampling (sampled_df 1K)"]
  D --> E["Persona Generation with CoT + Conditional Rules"]
  E --> F{"Mode Split"}
  F --> G1["MC Mode: Choose among products"]
  F --> G2["SW Mode: Switch from incumbent"]
  G1 --> H["Outputs: posterior.json, sampled_df.csv, personas_all.json, metrics"]
  G2 --> H
