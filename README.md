**Fully Connected Neural Network in Verilog – Module Overview**
<img width="1459" height="725" alt="image" src="https://github.com/user-attachments/assets/a3317f85-f8fb-47d1-8872-bfec71ae9e7e" />


Neuron Block

Performs:
y = ReLU(Σ (w_i * x_i) + b)

Components:

Multiply-Accumulate (MAC) units

Register for weights, inputs, bias

Optional ReLU logic

Output: 1 value per neuron

Layer Block

Consists of multiple neuron blocks in parallel

All neurons receive the same input vector, each with unique weights

Output: Vector of size equal to number of neurons
Hardmax Block

Takes a vector input and outputs one-hot encoding at index of max value

Steps:

1.Find max value and index

2. One-hot encode the index


**Top-Level Module
**
Connects:

Input → Layer 1 → ReLU → Layer 2 → ReLU → ... → Hardmax → Output

Controls:

Clock, reset, enable, valid/done signals

Weight and bias loading (from memory or file)
