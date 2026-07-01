# AI-Simulator

<img width="1864" height="900" alt="image" src="https://github.com/user-attachments/assets/9a1f1d35-d80f-4d51-af23-d6f8c36a33d9" />
<img width="1864" height="900" alt="image" src="https://github.com/user-attachments/assets/a62c2bb9-706f-4ac3-9a22-06342d417937" />

Here's what you're looking at:

**The concept — an artificial neuron**, the basic building block of a neural network. It's a simplified math model of how a biological neuron fires, and every layer in a deep learning model is just many of these wired together.

**What each piece in your screenshot means:**

- **Inputs (x₁–x₄)**: signals coming in — right now `1.00, -0.30, 0.90, 0.20`
- **Weights (w₁ⱼ–w₄ⱼ)**: how much importance/strength each input gets — `0.10, 0.50, -0.60, 0.40`. A negative weight (like w₃ⱼ) means that input actually *suppresses* the neuron rather than exciting it.
- **Σ (Transfer function)**: multiplies each input by its weight and adds them all up: `net input = Σ(xᵢ·wᵢ) = -0.51` (shown top right)
- **θⱼ (Threshold)**: a bias value that gets subtracted from that sum — it's the "how much evidence does this neuron need before it fires" knob
- **φ (Activation function)**: takes the net input and squashes/decides the final output. Since your net input is negative and you're likely on Step or a threshold-based function, the neuron isn't firing — output `oⱼ = 0.000`

**In plain terms:** the neuron is weighing four pieces of evidence, three "voting yes" and one "voting no" (w₃ⱼ = -0.60, paired with a strong x₃ = 0.90), and right now the "no" vote plus the small positive weights aren't enough to push the sum above zero — so the neuron stays silent (output 0). If you raise w₁ⱼ or w₂ⱼ, or make θⱼ more negative, you'd likely push it into firing.

This exact pattern — weight, sum, threshold, squash — repeats billions of times inside real neural networks like the ones behind image recognition or language models.
