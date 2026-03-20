# Multi-Layer Perceptrons Workshop

## Overview

[`MultiLayerPerceptrons_Workshop.ipynb`](MultiLayerPerceptrons_Workshop.ipynb) is a hands-on introduction to **neural networks** and **multi-layer perceptrons (MLPs)**. It moves from a single **perceptron** in NumPy through **activation functions**, **MLP architecture**, and **feedforward / backpropagation** theory, then trains the **same MLP architecture** on **MNIST** using **Keras**, **PyTorch**, and **TensorFlow (core API)**. The notebook ends with two completed challenges: a **framework comparison** and a **from-scratch NumPy** implementation with plots and reflection.

## Notebook contents

| Section | What you’ll find |
|--------|-------------------|
| **1–2** | Biological motivation; perceptron from scratch (NumPy) |
| **3** | Activation functions (sigmoid, tanh, ReLU) and plots |
| **4–5** | MLP structure; feedforward & backpropagation (conceptual + pseudocode) |
| **6** | **MNIST workshop**: data loading (Keras + PyTorch pipelines) |
| **Impl. 1–3** | Same architecture: **Keras** `Sequential`, **PyTorch** `nn.Module`, **TF** `keras.Model` + `GradientTape` |
| **Challenge 1** | Filled comparison: **speed**, **test accuracy**, **pros/cons**, answers on `val_accuracy` / `val_loss`, and notes on **fair comparisons** (e.g. PyTorch `Normalize` vs Keras/TF `[0,1]` pixels) |
| **Challenge 2** | Spec + **solution**: NumPy-only **2-hidden-layer + softmax** MLP, full **mini-batch epochs**, ReLU vs sigmoid, learning-rate plots, forward **activation** vs backward **\|dW\|** bars, **Mermaid** flow diagram, short **reflection** |
| **Summary** | Wrap-up of core ideas |

## Objectives

- See how a neuron combines inputs, weights, bias, and an activation.
- Understand why **nonlinear** activations and **multiple layers** matter.
- Train and evaluate an MLP on MNIST in **three** mainstream APIs.
- Relate high-level training loops to **manual** forward/backprop in NumPy.

## Running the notebook

1. **Python 3.10+** recommended (notebook metadata uses 3.11).
2. Create a venv and install dependencies, for example:
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Open `MultiLayerPerceptrons_Workshop.ipynb` in Jupyter or VS Code and run cells **top to bottom**.
4. **Challenge 2** code expects variables from the MNIST loading cell (`x_train_flat`, `y_train_tf`, `x_test_flat`, `y_test_tf`, etc.)—run that cell before the Challenge 2 solution.

Main libraries used in the notebook: **NumPy**, **Matplotlib**, **TensorFlow/Keras**, **PyTorch**, **torchvision** (MNIST download).

## Deliverables (as reflected in the notebook)

- Working **Keras / PyTorch / TensorFlow** MNIST classifiers and printed **test accuracy**.
- **Challenge 1**: completed comparison table and talking points.
- **Challenge 2**: commented NumPy implementation, experiment plots, diagram, and written reflection.

## Key takeaways

- The **same** MLP idea appears across frameworks; syntax and training loops differ.
- **Preprocessing** should match across frameworks when comparing metrics.
- **Backpropagation** is the chain rule applied layer-by-layer; NumPy code makes **gradients** and **activations** visible.

## Related files

- [`MultiLayeredPerceptrons.ipynb`](MultiLayeredPerceptrons.ipynb) — additional course-style notebook (if present in your clone).
- [`requirements.txt`](requirements.txt) — pinned environment from a local venv export (install may take a while due to TensorFlow/PyTorch).
