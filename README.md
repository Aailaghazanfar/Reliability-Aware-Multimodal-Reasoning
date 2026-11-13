
# Reliability-Aware Multimodal Reasoning

**Evaluating Modality-Specific Reliability Estimation in Vision-Language Models Under Conflicting Visual and Textual Evidence**

## Overview

Vision-Language Models (VLMs) process visual and textual information simultaneously. However, when these modalities provide conflicting evidence, a model may rely on misleading textual information instead of visual content.

This project investigates whether modality-specific reliability estimation can improve the decision-making of a frozen Vision-Language Model under controlled cross-modal conflicts.

## Research Question

Does modality-specific reliability estimation improve a VLM's ability to answer questions when visual and textual evidence conflict?

## Objectives

- Evaluate VLM performance under different visual and textual evidence conditions.
- Investigate how misleading textual information influences model responses.
- Examine modality-specific confidence and reliability indicators.
- Compare reliability-based decision strategies.
- Assess whether conflict-aware safeguards improve multimodal reasoning.

## Experimental Setup

| Component | Configuration |
|---|---|
| Model | Qwen/Qwen2-VL-2B-Instruct |
| Model training | Frozen (no fine-tuning) |
| Compute environment | Google Colab |
| GPU | NVIDIA Tesla T4 |
| Dataset | Controlled subset adapted from A-OKVQA validation split |
| Images | 18 |
| Questions | 18 |
| Experimental conditions | 4 |
| Total inference trials | 72 |

## Experimental Conditions

1. **IMAGE_ONLY:** Visual evidence without additional textual context.
2. **TRUE_TEXT:** Image with correct supporting textual evidence.
3. **MISLEADING_TEXT:** Image with deliberately misleading textual evidence.
4. **TEXT_ONLY:** Textual evidence without the image.

## Methodology

1. Benchmark preparation and controlled conflict construction.
2. Frozen VLM inference across four experimental conditions.
3. Extraction of token-level confidence indicators.
4. Modality-specific reliability assessment.
5. Comparison of confidence-based and conflict-aware decision strategies.
6. Statistical analysis of experimental outcomes.

## Results

The repository includes experimental inference results, confidence and uncertainty analysis, statistical comparisons, reliability strategy evaluation, and visualizations.

Detailed numerical findings will be documented in the research report and results files.

## Limitations

- The benchmark contains a relatively small controlled sample of 18 image-question pairs.
- Findings are specific to the evaluated model and experimental setup.
- Confidence indicators do not necessarily represent calibrated probabilities of answer correctness.
- Results should not be interpreted as evidence of general VLM reliability across all tasks.

## Reproducibility

The notebooks and supporting files document the experimental workflow. Model weights are not included. The pretrained model is identified by its Hugging Face model ID.

## Acknowledgements

This project uses Qwen2-VL and draws on the A-OKVQA benchmark.

Original dataset and model licenses and citations should be consulted before reuse.

## Responsible AI

This research investigates multimodal reasoning reliability and the potential effects of conflicting evidence. Findings are limited to the controlled benchmark and should not be interpreted as clinical or other high-stakes deployment validation.
