# Neural Network Components and Learning Process

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

Neural networks learn patterns by passing data through connected layers of neurons. This artifact uses a **circle classification** example to show what each component does and how the network improves its predictions during training.

<div class="nn-intro"><div class="nn-eyebrow">AIML-501 · Model Development · Portfolio Artifact</div><div class="nn-intro-title">Seeing how a neural network learns</div><p>From input features to a prediction, then from loss back to better weights.</p><a class="nn-cta" href="../assets/aiml-501-neural-network-slides.html">Open the visual presentation ↗</a> <a class="nn-inline-link" href="https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.68981&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false">Open the TensorFlow Playground configuration ↗</a></div>

---

## Description

This visual walkthrough explains **layers, neurons, weights, activation functions, loss functions, and optimization algorithms**. The example is a neural network with two inputs, a 4-neuron hidden layer, a 2-neuron hidden layer, and one classification output. Diagrams and concise explanations connect the architecture to the learning process.

---

## Objective

The goal is to make the building blocks of a neural network understandable through an actual model configuration, and to explain why a nonlinear network can learn to distinguish points inside a circle from points outside it.

---

## Process

I selected the circle classification dataset in TensorFlow Playground, using two input features (X₁ and X₂), the **Tanh** activation function, a learning rate of **0.03**, and a **4 → 2** hidden-layer configuration. I then mapped each network component to its role in making predictions and updating parameters. The presentation also lays out controlled experiments to compare noise and layer depth.

The saved Playground link records the **configuration**, not measured training results. Training and test loss must be read from a completed run; the diagrams on this page are illustrative.

---

## Tools and Technologies Used

- TensorFlow Playground for configuring and exploring a small neural network
- PowerPoint for designing a visual presentation
- GitHub Pages, Markdown, HTML, and CSS for the portfolio version
- ChatGPT to help organize and format explanations and visual schematics

---

## Key Concepts Learned

The input layer passes feature values forward. **Hidden layers** transform those values, while **neurons** compute weighted sums, add biases, and apply activations. **Weights** control connection strength; **Tanh** adds the nonlinearity needed for a curved decision boundary. A **loss function** measures prediction error, while a gradient-based **optimizer** uses backpropagation gradients to adjust trainable parameters.

For this circle problem, using only X₁ and X₂ keeps the inputs simple. The challenge lies in learning a nonlinear relationship rather than drawing a single straight separating line.

---

## Value Proposition

### Unique Value

Instead of memorizing definitions, this artifact shows the six components working together within one specific 2 → 4 → 2 → 1 network. It connects network structure, prediction, and feedback in an easy-to-follow visual.

### Relevance

These ideas apply to larger deep learning models used for image recognition, language processing, forecasting, and anomaly detection. Understanding the basics makes it easier to reason about capacity, model complexity, generalization, and training behavior.

---

## Artifact Evidence

<style>
.nn-intro{background:linear-gradient(120deg,#102b46,#20588c);border-radius:14px;color:#fff;padding:27px 29px;margin:20px 0 26px;box-shadow:0 8px 24px rgba(16,43,70,.14)}
.nn-eyebrow{text-transform:uppercase;letter-spacing:1.6px;color:#97eddd;font-size:11px;font-weight:700}
.nn-intro-title{font-size:29px;font-weight:800;line-height:1.14;margin:10px 0}
.nn-intro p{color:#e7f3ff;margin:0 0 20px}
.nn-cta{display:inline-block;background:#21b9ad;color:#072b37!important;border-radius:9px;text-decoration:none!important;padding:10px 14px;font-weight:700;margin:4px 12px 4px 0}
.nn-inline-link{color:#e1f8ff!important;text-decoration:underline}
.nn-shell{border:1px solid #dce5ef;background:linear-gradient(180deg,#fbfdff,#f1f6fb);border-radius:15px;padding:17px 15px;margin:17px 0}
.nn-shell svg{display:block;width:100%;height:auto}
.nn-strip{display:flex;flex-wrap:wrap;gap:8px;margin:13px 0}
.nn-chip{background:#e9f2fb;border:1px solid #d6e4f3;border-radius:20px;color:#21436b;font-size:12px;font-weight:700;padding:7px 11px}
.nn-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:13px;margin:18px 0}
.nn-card{padding:18px;border-radius:12px;border:1px solid #dce6f0;background:#fff;box-shadow:0 3px 12px rgba(35,58,80,.06)}
.nn-card h3{margin:0 0 8px;color:#163958;font-size:17px}.nn-card p{font-size:13px;line-height:1.65;color:#39516b;margin:0}
.nn-index{display:inline-block;color:#306eaa;background:#ecf5ff;border-radius:6px;padding:3px 8px;font-size:11px;font-weight:700;margin-bottom:8px}
.nn-cycle{display:flex;flex-wrap:wrap;gap:9px;align-items:center;margin:18px 0}
.nn-step{flex:1 1 130px;padding:14px 11px;background:#ecf6f8;border:1px solid #bfdee3;border-radius:10px;text-align:center;color:#13566c;font-weight:700;font-size:13px}
.nn-note{padding:13px 15px;border-left:4px solid #d39734;background:#fff9ed;color:#62481d;border-radius:5px;font-size:13px;margin:18px 0}
@media(max-width:640px){.nn-grid{grid-template-columns:1fr}.nn-intro{padding:19px}.nn-intro-title{font-size:24px}.nn-shell{padding:9px}.nn-step{flex:1 1 100%}}
</style>

### 1. Network architecture

<div class="nn-shell"><svg viewBox="0 0 770 345" role="img" aria-label="Neural network with two input features, four neurons in hidden layer one, two in hidden layer two, and one output neuron."><line x1="108" y1="150" x2="267" y2="105" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="150" x2="267" y2="165" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="150" x2="267" y2="225" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="150" x2="267" y2="285" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="260" x2="267" y2="105" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="260" x2="267" y2="165" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="260" x2="267" y2="225" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="108" y1="260" x2="267" y2="285" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="105" x2="467" y2="165" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="105" x2="467" y2="245" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="165" x2="467" y2="165" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="165" x2="467" y2="245" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="225" x2="467" y2="165" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="225" x2="467" y2="245" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="285" x2="467" y2="165" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="303" y1="285" x2="467" y2="245" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="503" y1="165" x2="662" y2="205" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><line x1="503" y1="245" x2="662" y2="205" stroke="#91a5bd" stroke-width="1.35" opacity=".4"/><circle cx="90" cy="150" r="21" fill="#10b5b1" stroke="#fff" stroke-width="4"/><text x="90" y="155" fill="#fff" text-anchor="middle" font-size="15" font-weight="700">X1</text><circle cx="90" cy="260" r="21" fill="#10b5b1" stroke="#fff" stroke-width="4"/><text x="90" y="265" fill="#fff" text-anchor="middle" font-size="15" font-weight="700">X2</text><circle cx="285" cy="105" r="21" fill="#5b85eb" stroke="#fff" stroke-width="4"/><text x="285" y="110" fill="#fff" text-anchor="middle" font-size="15" font-weight="700"></text><circle cx="285" cy="165" r="21" fill="#5b85eb" stroke="#fff" stroke-width="4"/><text x="285" y="170" fill="#fff" text-anchor="middle" font-size="15" font-weight="700"></text><circle cx="285" cy="225" r="21" fill="#5b85eb" stroke="#fff" stroke-width="4"/><text x="285" y="230" fill="#fff" text-anchor="middle" font-size="15" font-weight="700"></text><circle cx="285" cy="285" r="21" fill="#5b85eb" stroke="#fff" stroke-width="4"/><text x="285" y="290" fill="#fff" text-anchor="middle" font-size="15" font-weight="700"></text><circle cx="485" cy="165" r="21" fill="#805bce" stroke="#fff" stroke-width="4"/><text x="485" y="170" fill="#fff" text-anchor="middle" font-size="15" font-weight="700"></text><circle cx="485" cy="245" r="21" fill="#805bce" stroke="#fff" stroke-width="4"/><text x="485" y="250" fill="#fff" text-anchor="middle" font-size="15" font-weight="700"></text><circle cx="680" cy="205" r="21" fill="#e79b3a" stroke="#fff" stroke-width="4"/><text x="680" y="210" fill="#fff" text-anchor="middle" font-size="15" font-weight="700">ŷ</text><g font-size="14" font-weight="700" fill="#2a4059" text-anchor="middle"><text x="90" y="48">Input</text><text x="285" y="48">Hidden 1</text><text x="485" y="48">Hidden 2</text><text x="680" y="48">Output</text></g><g font-size="12" fill="#536780" text-anchor="middle"><text x="90" y="68">2 features</text><text x="285" y="68">4 neurons</text><text x="485" y="68">2 neurons</text><text x="680" y="68">1 score</text></g></svg></div>

<div class="nn-strip"><span class="nn-chip">Circle classification</span><span class="nn-chip">2 → 4 → 2 → 1</span><span class="nn-chip">Tanh</span><span class="nn-chip">Learning rate: 0.03</span><span class="nn-chip">Batch size: 10</span><span class="nn-chip">Noise: 0</span><span class="nn-chip">50% training data</span></div>

### 2. Six components, one learning system

<div class="nn-grid">
<div class="nn-card"><div class="nn-index">01 · STRUCTURE</div><h3>Layers</h3><p>Inputs enter the network; hidden layers progressively transform them; the output layer produces a classification score.</p></div>
<div class="nn-card"><div class="nn-index">02 · COMPUTATION</div><h3>Neurons</h3><p>Each neuron combines its inputs, adds a bias, and applies an activation: a = tanh(Σwᵢxᵢ + b).</p></div>
<div class="nn-card"><div class="nn-index">03 · PARAMETERS</div><h3>Weights</h3><p>Learnable values on connections control how much each incoming signal contributes. Biases shift the neuron's response.</p></div>
<div class="nn-card"><div class="nn-index">04 · NONLINEARITY</div><h3>Activation functions</h3><p>Tanh maps values between −1 and +1 and allows hidden layers to represent nonlinear patterns, including curved boundaries.</p></div>
<div class="nn-card"><div class="nn-index">05 · FEEDBACK</div><h3>Loss functions</h3><p>Loss measures how different predictions are from the correct labels. Lower loss generally means a better fit to those examples.</p></div>
<div class="nn-card"><div class="nn-index">06 · LEARNING</div><h3>Optimization algorithms</h3><p>Gradient-based optimization uses error gradients computed through backpropagation to update weights and biases.</p></div>
</div>

### 3. How training works

<div class="nn-cycle"><div class="nn-step">1. Forward pass<br>Predict</div><div class="nn-step">2. Loss<br>Measure error</div><div class="nn-step">3. Backpropagation<br>Compute gradients</div><div class="nn-step">4. Optimization<br>Update weights</div></div>

The network repeats this cycle over batches of examples. Training loss reflects fit to the training examples; test loss helps reveal how well the network generalizes to examples not used for parameter updates.

### 4. Controlled experiments

| Experiment | Setting to change | What to compare |
|---|---|---|
| Baseline | Tanh, hidden layers 4 and 2, noise 0 | Decision boundary and training/test loss after training |
| Noisy data | Increase noise from 0 to about 20 | Whether the classes become harder to separate |
| Network depth | Compare one hidden layer with two | Boundary shape, training behavior, and loss |

<div class="nn-note"><strong>Experiment evidence:</strong> The linked Playground configuration does not store a completed training run. Record your own epoch count and training/test loss, and capture screenshots before claiming specific performance results.</div>

### 5. Full visual presentation

The presentation arranges the architecture, core components, Tanh, loss, optimization, and takeaways as a slide-style visual story.

<a class="nn-cta" href="../assets/aiml-501-neural-network-slides.html">View the 12-slide presentation ↗</a>

[Open the interactive TensorFlow Playground experiment](https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.68981&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false)

---

## Summary and Reflection

Making the network visual helped me understand how the individual parts fit together. The layers define the flow of information, weights and activation functions shape the predictions, and the loss function gives the optimizer the feedback needed to improve. For the circle example, the main insight is that nonlinear transformations let a model learn a boundary that a single straight-line classifier cannot represent. Visualizing the model also makes it easier to think about the effect of changing features, noise, or hidden layers.

---

## References

1. [TensorFlow Playground](https://playground.tensorflow.org/) — interactive neural network visualization and training tool.
2. [TensorFlow: Neural networks](https://www.tensorflow.org/guide/keras/sequential_model) — model layers and sequential computation.
3. Indiana Wesleyan University, AIML-501 Model Development course instructions and workshop resources.

---

[Back to AIML-501 — Model Development](/parin-ai-portfolio/aiml-501)
