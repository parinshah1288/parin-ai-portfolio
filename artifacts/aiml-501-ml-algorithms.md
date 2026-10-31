# Machine Learning Algorithms Visual Framework

<nav aria-label="Main navigation" style="display:flex;align-items:center;justify-content:center;gap:22px;flex-wrap:wrap;margin:22px auto;padding:12px 16px;border-top:1px solid #e3e8ef;border-bottom:1px solid #e3e8ef;">
  <a href="/parin-ai-portfolio/" style="font-weight:600;text-decoration:none;">Home</a>
  <a href="/parin-ai-portfolio/about" style="font-weight:600;text-decoration:none;">About</a>
  <details style="display:inline-block;position:relative;">
    <summary style="cursor:pointer;font-weight:600;list-style:revert;">Courses</summary>
    <div style="position:absolute;top:100%;right:0;z-index:1000;min-width:270px;background:#fff;border:1px solid #dce3eb;border-radius:8px;box-shadow:0 6px 18px rgba(0,0,0,.14);padding:12px 15px;text-align:left;">
      <a href="/parin-ai-portfolio/aiml-501" style="display:block;padding:8px 0;white-space:nowrap;">AIML-501 — Model Development</a>
      <a href="/parin-ai-portfolio/aiml-500" style="display:block;padding:8px 0;white-space:nowrap;">AIML-500 — Machine Learning Fundamentals</a>
    </div>
  </details>
</nav>

---

## Introduction

Machine learning algorithms solve different kinds of problems. Some predict an answer using examples that already have labels, some discover patterns in unlabeled data, and others learn to generate entirely new text or images. This visual guide compares **10 widely used methods and model families** to help explain when each is useful.

---

## Description

This artifact contains a visual overview of ten methods, grouped by learning approach, along with a domain comparison and an explanation of why each method was classified as shown. Every method has a brief explanation and one practical use case.

---

## Objective

The goal of this artifact is to organize key machine learning methods by **learning approach**, **application domain**, and **practical purpose**. It covers tabular data, computer vision, natural language processing (NLP), and generative AI.

---

## Process

To develop the framework, I first identified representative traditional ML algorithms and modern generative model families. I compared their training objectives and then mapped each method to the problem areas where it is commonly applied. Finally, I added brief examples—primarily from equipment monitoring, manufacturing, technical support, and content generation—to make the concepts easier to connect to real applications. The presentation was organized as a website-native visual framework so readers can browse it on desktop or mobile.

---

## Tools and Technologies Used

- GitHub Pages and Markdown for hosting and documenting the portfolio artifact
- HTML and CSS for the visual layout and responsive cards
- Course materials and linked reference documentation
- ChatGPT as an assistance tool for organizing, explaining, and formatting the content; technical decisions and examples should be reviewed before submission

---

## Key Concepts Learned

I organized the methods using **two separate dimensions**. The first is the learning objective: whether a system is trained on labeled answers, discovers patterns from unlabeled examples, or learns to generate content. The second is the **application domain**, such as structured tables, images, or language. These dimensions are related but not interchangeable: a computer vision model describes *where it is used*, while supervised learning describes *how it learns*.

For supervised learning, Linear Regression is suited to numerical predictions; Decision Trees give readable decision rules; Random Forests combine many trees to improve generalization; and SVMs separate classes using a margin. CNNs are usually taught using labeled images, but **a CNN is a neural-network architecture, not a learning style**, so it can also be trained with other objectives.

K-means and PCA are placed under unsupervised learning because neither needs target labels for its primary task. They do different jobs: **K-means groups similar observations**, while **PCA compresses features by preserving as much variance as possible**. PCA may also be used before a supervised model.

For generative AI, a simple supervised-versus-unsupervised label would hide important differences. GPT-style language models commonly use **self-supervised next-token prediction** during pretraining, sometimes followed by supervised fine-tuning. GANs learn through a generator–discriminator objective and may be unconditional or conditional. Diffusion models often learn to remove deliberately added noise and can be conditioned on text or other inputs. These are **generative model families with different training objectives**, rather than a single learning category.

- **Decision Tree → Random Forest:** a forest combines multiple decision trees instead of relying on just one.
- **PCA → SVM or another predictor:** PCA can reduce dimensions before a supervised classifier is trained.
- **CNN ↔ GAN / Diffusion:** convolutional networks can be components within image-generation systems, although modern architectures may also use attention.
- **GPT-style Transformers, GANs, and diffusion models:** all can generate content, but their architectures and training objectives differ.
- **Tabular, vision, NLP, and generative AI are not mutually exclusive:** a method can cover several domains.

| Domain | Useful approaches from this framework | Example goal |
|---|---|---|
| **Tabular data** | Linear Regression, Decision Tree, Random Forest, SVM, K-means, PCA | Forecast cost, predict failures, segment equipment, reduce sensor features |
| **Computer vision** | CNN, SVM on image features, GAN, Diffusion Model | Inspect images, detect defects, create synthetic images |
| **NLP** | GPT-style Transformer, SVM on text features | Summarize technical reports, classify support requests |
| **Generative AI** | GPT-style Transformer, GAN, Diffusion Model | Create reports, synthetic images, or visual concepts |

---

## Value Proposition

This guide is a quick reference for students and engineers who need to select a sensible starting point for an ML problem. It shows that model selection should begin with the data available and the outcome needed—not simply with whichever algorithm is popular.

### Unique Value

The examples emphasize engineering operations such as factory sensors, equipment reliability, image-based inspection, and technical documentation. This connects foundational machine learning ideas with the kinds of data-intensive systems used in industry.

### Relevance

Understanding differences between prediction, clustering, feature reduction, and generation is important when designing real-world AI applications. The framework also highlights that **learning style, architecture, and application domain are different classification axes**—a distinction that matters when comparing modern generative AI methods.

---

## Artifact Evidence

<style>
.ml-figure{font-family:Arial,Helvetica,sans-serif;margin:18px 0 26px;color:#203047}
.ml-lead{background:#163958;color:#fff;border-radius:13px;padding:20px 22px;text-align:center}
.ml-lead h2{color:#fff;margin:0 0 7px;font-size:23px}.ml-lead p{margin:0;color:#eef6ff;font-size:14px}
.ml-branches{text-align:center;color:#657a91;font-size:28px;line-height:1.4}
.ml-group{border-radius:12px;padding:14px 15px;margin:16px 0;border:1px solid #dce4ec;background:#f8fafc}
.ml-group.super{border-left:6px solid #2176ae}.ml-group.unsuper{border-left:6px solid #25836f}.ml-group.gen{border-left:6px solid #7659b2}
.ml-group header h3{margin:0 0 4px;font-size:19px;color:#163958}.ml-group header p{margin:0 0 12px;color:#53647a;font-size:13px}
.ml-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px}
.ml-card{background:#fff;border:1px solid #e1e7ee;border-radius:10px;padding:14px;box-shadow:0 2px 5px rgba(17,45,74,.05);min-width:0}
.ml-top{display:flex;align-items:center;gap:9px;margin-bottom:7px;color:#1b3550}.ml-num{background:#e6edf6;color:#31577d;padding:5px 7px;font-weight:700;border-radius:5px;font-size:12px}
.ml-tag{font-size:11px;font-weight:bold;color:#32496c;background:#edf2f8;border-radius:20px;padding:4px 9px;display:inline-block;margin-bottom:5px}
.ml-card p{font-size:12px;line-height:1.55;margin:6px 0;color:#344557}
.ml-key{display:flex;gap:12px;flex-wrap:wrap;margin:15px 0;font-size:12px;color:#425267}
.ml-key span{padding:7px 10px;border:1px solid #e0e6ed;border-radius:6px;background:#fff}
@media(max-width:640px){.ml-grid{grid-template-columns:1fr}.ml-lead h2{font-size:20px}.ml-group{padding:11px}.ml-card{padding:12px}}
@media print{.ml-group,.ml-card{break-inside:avoid}.ml-card{box-shadow:none}}
</style>

<div class="ml-figure" role="group" aria-label="A framework of ten machine learning algorithms grouped by training approach, with application domains, explanations and examples">
<div class="ml-lead"><h2>Machine Learning: Choosing the Right Approach</h2><p>Learning approach → algorithm or model family → application domain → practical use</p></div>
<div class="ml-branches" aria-hidden="true">↓</div>
<section class="ml-group super"><header><h3>Supervised learning</h3><p>Predictions from examples with known answers</p></header><div class="ml-grid"><article class="ml-card"><div class="ml-top"><span class="ml-num">01</span><strong>Linear Regression</strong></div><div class="ml-tag">Supervised</div><p><b>Domains:</b> Tabular data</p><p><b>How it works:</b> Predicts a number by fitting a line or linear relationship between input features and a target.</p><p><b>Real-world use:</b> Estimate equipment maintenance cost using machine age and operating hours.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">02</span><strong>Decision Tree</strong></div><div class="ml-tag">Supervised</div><p><b>Domains:</b> Tabular data</p><p><b>How it works:</b> Splits data using a series of feature-based questions until it reaches a prediction.</p><p><b>Real-world use:</b> Identify potentially defective factory components from sensor readings.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">03</span><strong>Random Forest</strong></div><div class="ml-tag">Supervised</div><p><b>Domains:</b> Tabular data</p><p><b>How it works:</b> Combines predictions from many decision trees trained on varied samples and features.</p><p><b>Real-world use:</b> Predict equipment failure from historical telemetry and maintenance records.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">04</span><strong>Support Vector Machine (SVM)</strong></div><div class="ml-tag">Supervised</div><p><b>Domains:</b> Tabular data; computer vision; NLP</p><p><b>How it works:</b> Finds a separating boundary with a large margin between classes; kernels support nonlinear boundaries.</p><p><b>Real-world use:</b> Classify spam messages or detect product defects from extracted image features.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">05</span><strong>Convolutional Neural Network (CNN)</strong></div><div class="ml-tag">Usually supervised; can also be self-supervised</div><p><b>Domains:</b> Computer vision</p><p><b>How it works:</b> Uses learned convolutional filters to recognize spatial features, progressing from edges to complex shapes.</p><p><b>Real-world use:</b> Recognize damaged parts in photos from a manufacturing line.</p></article></div></section>
<section class="ml-group unsuper"><header><h3>Unsupervised learning</h3><p>Patterns and structure without target labels</p></header><div class="ml-grid"><article class="ml-card"><div class="ml-top"><span class="ml-num">06</span><strong>K-means Clustering</strong></div><div class="ml-tag">Unsupervised</div><p><b>Domains:</b> Tabular data; computer vision features</p><p><b>How it works:</b> Groups similar data points into K clusters by repeatedly updating cluster centers.</p><p><b>Real-world use:</b> Group manufacturing tools by similar performance patterns without preset labels.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">07</span><strong>Principal Component Analysis (PCA)</strong></div><div class="ml-tag">Unsupervised</div><p><b>Domains:</b> Tabular data; image features</p><p><b>How it works:</b> Finds directions of greatest variation so data can be represented with fewer dimensions.</p><p><b>Real-world use:</b> Reduce hundreds of correlated sensor measurements before visualization.</p></article></div></section>
<section class="ml-group gen"><header><h3>Generative and self-supervised approaches</h3><p>Producing content; training objectives vary</p></header><div class="ml-grid"><article class="ml-card"><div class="ml-top"><span class="ml-num">08</span><strong>GPT-style Transformer</strong></div><div class="ml-tag">Primarily self-supervised pretraining; often supervised fine-tuning</div><p><b>Domains:</b> NLP; generative AI</p><p><b>How it works:</b> Learns token relationships with attention and generates text by predicting subsequent tokens.</p><p><b>Real-world use:</b> Draft summaries of service incidents or answer questions over technical documentation.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">09</span><strong>Generative Adversarial Network (GAN)</strong></div><div class="ml-tag">Generative; typically unsupervised or conditional training</div><p><b>Domains:</b> Computer vision; generative AI</p><p><b>How it works:</b> Trains a generator and discriminator against each other so generated samples become more realistic.</p><p><b>Real-world use:</b> Create synthetic defect images to augment a vision training dataset.</p></article>
<article class="ml-card"><div class="ml-top"><span class="ml-num">10</span><strong>Diffusion Model</strong></div><div class="ml-tag">Generative; commonly self-supervised denoising training</div><p><b>Domains:</b> Computer vision; generative AI</p><p><b>How it works:</b> Learns to remove noise step by step, then generates data from noise, sometimes guided by text.</p><p><b>Real-world use:</b> Generate concept images or synthetic visual examples for prototyping.</p></article></div></section>
<div class="ml-key"><span>🔵 Supervised: labeled examples</span><span>🟢 Unsupervised: structure without target labels</span><span>🟣 Generative: creating new content (training varies)</span></div>
</div>

**How to read the framework:** Start with what you need to do: predict a known outcome, uncover hidden structure, or generate new content. Then compare the model families in that group. Application domains overlap—a single method can be used in more than one domain.

---

## References

1. Indiana Wesleyan University, AIML-501 course instructions and course learning resources.
2. [scikit-learn: Supervised Learning](https://scikit-learn.org/stable/supervised_learning.html)
3. [scikit-learn: Unsupervised Learning](https://scikit-learn.org/stable/unsupervised_learning.html)
4. [Hugging Face Transformers: Tasks and Models](https://huggingface.co/docs/transformers/index)
5. [Hugging Face Diffusers: Training Overview](https://huggingface.co/docs/diffusers/training/overview)
6. [Goodfellow et al. (2014): Generative Adversarial Networks](https://arxiv.org/abs/1406.2661)

---

[Back to AIML-501 — Model Development](/parin-ai-portfolio/aiml-501)
