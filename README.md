# Competing Circuits Across Languages
> ⚠️ Work in Progress — Phase 1 PoC

## Phase 1 (Proof of Concept) - bloom-560m, 8 pairs
Key finding: JA/EN variance ratio 2.3 in jailbreak category

### Dataset
- 4 categories: direct_harm, jailbreak, ambiguous, benign
- 8 pairs × 2 languages (EN/JA) = 16 entries
- Model: bloom-560m (no safety finetuning)

### Variance Ratio Calculation
- Averaged hook_resid_post at Layer 6, 12, 18 across token positions
- Computed var→mean across prompts within each category
- JA/EN ratio: jailbreak 2.3, benign 1.0, direct_harm 0.04
