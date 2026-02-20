## TrustMH_Bench

**TrustMH_Bench** is a benchmark for evaluating **general-purpose LLMs** and **mental-health-specific LLMs (MH-LLMs)** across multiple trust-related dimensions.

This repository organizes the 8 dimensions into two groups and provides a unified interface to run different models.

---

## Repository Structure

```text
TrustMH_Bench/
  DimGroup1/                 # First 4 dimensions, general vs MH-LLM code separated
    General-model/           # Evaluation code for general-purpose LLMs
      fair/
      privacy/
      reliability/
      security_for_jailbreak/
    MH-LLM/                  # Evaluation code for MH-LLMs
      1.23/
      code/

  DimGroup2/                 # Last 4 dimensions, shared framework for all models
    Crisis Identification and Escalation/
      C-SSRS/
      LLMs-Mental-Health-Crisis/
    Ethics/
    Robustness/
    Sycophancy/

  specific_model_response/   # Common interface to run specific MH-LLMs
    data/
    LLMs/
      BaseLLM.py
      MentalLLaMA.py
      Meditron.py
      PsycoLLM.py
      Simpsybot.py
      SoulChat.py
      Llama2.py
    output/
    run_inference.py
```

---

## Usage

- Use code under `DimGroup1/General-model/` to evaluate **general LLMs** on the first four dimensions.
- Use code under `DimGroup1/MH-LLM/` and `DimGroup2/` together with `specific_model_response/` to evaluate **MH-LLMs** and compare them with general LLMs.
- For each dimension, refer to the corresponding subdirectory for scripts and configuration details.

