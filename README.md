# Custom-Neural-Network
This code represents a journey from implementing fundamental mathematical operations and graph-based computation (manual backpropagation) to building a modular neural network structure, followed by an implementation of a simple multi-layer perceptron (MLP) with training functionality.

Below is a description of what this code does:

1. Gradient Calculation Basics:
The Value class is defined to store data, its gradient (grad), and methods for backpropagation.
Operations like addition, multiplication, subtraction, and activation functions (tanh, exp) are overloaded for Value objects, enabling auto-differentiation through computation graphs.
Backpropagation is manually implemented by defining _backward functions for every operation and then traversing the graph in reverse order.
2. Visualization of Computation Graph:
Using the graphviz library, a computation graph is drawn to visualize how inputs and operations are linked.
This is useful for debugging and understanding how gradients flow through the network.
3. Implementing Forward and Backward Pass:
Small manual neural network operations are performed using tensors (torch) and the Value class.
Examples include computing the output of a simple neuron and using .backward() to calculate gradients.
4. Building a Modular Neural Network:
Neuron class: Represents a single neuron with weights, biases, and the tanh activation.
Layer class: Represents a layer consisting of multiple neurons.
MLP class: Represents a multi-layer perceptron, constructed using the Layer class.
Forward passes are implemented using the __call__ method, enabling seamless computation.
5. Training the MLP:
The MLP is trained using a small dataset (xs as input and ys as the desired target).
For each training iteration:
Forward pass: Compute predictions for all inputs.
Loss calculation: Mean squared error is used as the loss function.
Backward pass: Gradients are computed and propagated through the network.
Parameter update: Gradient descent is used to adjust weights and biases.
6. Training Results:
The loss value decreases over iterations, showing that the MLP learns to minimize the error by adjusting parameters.
