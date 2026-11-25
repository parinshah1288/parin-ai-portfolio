# Assignment 5.4 — Explanatory Note

[Return to the model selection artifact](/parin-ai-portfolio/artifacts/aiml-501-model-selection-explainability)

**AIML-501 · Workshop Five · November 25, 2026**

## Purpose

This graphic compares five documented pre-trained models from three domains: all-MiniLM-L6-v2 and all-mpnet-base-v2 (NLP embeddings), MobileNetV3 Large and EfficientNet-B0 (vision), and TabPFN-v2 (tabular classification). It evaluates model size, source-reported predictive performance, throughput or computational cost, and explainability.

## Visual decision matrix

<figure style="margin:20px 0;">
  <a href="/parin-ai-portfolio/assets/aiml-501-model-selection-matrix.svg"><img src="/parin-ai-portfolio/assets/aiml-501-model-selection-matrix.svg" alt="Decision matrix comparing MiniLM, MPNet, MobileNetV3 Large, EfficientNet-B0 and TabPFN-v2 by model size, benchmark quality, inference speed or compute, and explainability." style="display:block;width:100%;height:auto;border:1px solid #dbe6ee;border-radius:12px;"></a>
  <figcaption style="font-size:0.85rem;color:#526779;text-align:center;margin-top:10px;">Figure 1. Pre-trained model selection matrix across NLP, computer vision, and tabular classification. Select the graphic to view it at full size.</figcaption>
</figure>

## Research method

I used published model-card data from Sentence Transformers and TorchVision, the peer-reviewed TabPFN study in *Nature*, and Prior Labs' comparative technical report. This is a research synthesis, not a newly run experiment. Each quality figure retains its original units: semantic-search aggregate score, ImageNet-1K top-1 accuracy, or dataset-level tabular results. Throughput, GFLOPs, and scenario-specific inference latency are separate measurements and should not be ranked as if they were interchangeable.

## Main findings

For language, MiniLM (22.7M parameters; reference speed 14,200 sentences/s) offers a smaller high-throughput embedding model. MPNet (109M; 2,800 sentences/s) achieves a higher reported aggregate semantic-search score (57.02 vs. 49.54). For vision, MobileNetV3 Large requires fewer operations (0.22 GFLOPs/image) while EfficientNet-B0 has higher reported ImageNet-1K top-1 accuracy (77.692% vs. 75.274%; 0.39 GFLOPs). For tabular prediction, TabPFN-v2 has strong small-data results but conditional inference cost: the original study reports about 0.2 seconds for one GPU prediction with 10,000 rows and 10 features. A fitted CatBoost or XGBoost baseline remains important.

## Explainability, deployment, and design

For embeddings, examine retrieval examples and perturbation tests; for vision, examine Grad-CAM and saliency overlays; for tabular predictions, use permutation importance, SHAP-style attribution, and counterfactual checks. These tools diagnose behavior but do not prove causation. Before launch, benchmark candidates on held-out target data and production hardware, evaluate subgroup errors and calibration, measure p95 latency and peak memory, review licensing, and monitor drift.

The design organizes five models under the same five headings—domain, size, quality, speed/compute, and explainability. Teal, purple, and orange distinguish NLP, vision, and tabular data. A full accessible table and references accompany the graphic so the information can be checked and read without relying on color alone.

## References

- Sentence Transformers. (n.d.). *Pretrained models*. https://www.sbert.net/docs/sentence_transformer/pretrained_models.html
- Sentence Transformers. (n.d.). *Model performance table*. https://github.com/huggingface/sentence-transformers/blob/main/docs/_static/html/models_en_sentence_embeddings.html
- PyTorch. (n.d.). *Models and pre-trained weights*. https://docs.pytorch.org/vision/main/models.html
- Hollmann, N., et al. (2025). Accurate predictions on small data with a tabular foundation model. *Nature, 637*, 319–326. https://doi.org/10.1038/s41586-024-08328-6
- Prior Labs. (2026). *TabPFN-3 technical report*. https://arxiv.org/abs/2605.13986

**AI-use disclosure:** AI assistance supported research organization and artifact formatting; claims were checked against the cited references. No new empirical benchmarks are claimed.
