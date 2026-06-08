# Multilayer Perceptron (from scratch)

A perceptron is a fundamental component of artificial neural networks. Inspired by the neurons in our brains*, these perceptrons make decisions and "learn" by iterating to minimize errors. When these single perceptrons are combined in layers, they form networks that can "learn" more complex patterns and make more nuanced decisions.

**Organic neurons can have different purposes, and more neurons do not necessarily mean more intelligence. I think this is really interesting because this is very similar to how artificial neurons work.*
  <br>***Fun Fact:** The African elephant brain has 257 billion neurons which is 3x the human brain. - https://pmc.ncbi.nlm.nih.gov/articles/PMC4053853/*
  
In an attempt to grasp these mechanisms more thoroughly, I decided to create my own simple multilayer perceptron (MLP) and compute everything by hand (using a calculator). This process gave me a more confident and comprehensive understanding of this concept, which I can lean on when dealing with more complex systems. This process also helped to demystify AI and has given me a greater appreciation for the computing power of modern computers.

## Full Notebook
![Full Notebook](./screenshots/0.Full.png)

## Architecture
When building an MLP, one of the first decisions that has to be made is the architecture. In other words, how many layers of perceptrons, how many perceptrons in each layer, and the connections between the perceptrons. Since I am doing all these calculations manually, I wanted to keep the architecture simple. Here I have what looks like a fully conected 3 layer network, but is functionally just 2 layers, given that the input layer doesn't contain any parameters, just passes the inputs to the next layer. The hidden layer learns the patterns in the data and passes its own version of input information to the output layer, which has the responsibility of making the prediction. In a deeper network, the first hidden layers learn more surface-level patterns while the deeper layers learn the complex and specific patterns in the data. 

The learning process that was mentioned earlier involves updating parameters (weights and biases) to minimize loss. These parameters were randomly chosen values between 0 and 1, again to make calculations easier.
![Architecture](./screenshots/1.Architecture.png)

## 1st Forward Pass
### Step 1: Compute weighted sum
The first forward pass will net the first prediction, which will start the learning process. Here in step 1, you calculate the hidden neurons by multiplying the inputs by the weights that connect those inputs to the hidden neuron and then adding the bias associated to the hidden neuron. The weights are used to distribute the importance of certain inputs to the neuron. This is useful, for example, if you are trying to find the difference between a tulip and a rose, one hidden neuron could roughly be responsible for detecting color, and another neuron could focus on the petal shape. If the inputs are the RGB values and petal length and width, then RGB should account for more decision-making power in hidden neuron 1, and length and width should account for more in hidden neuron 2. The weights will make those distributions accordingly. The biases are also useful for setting the baseline for each neuron. If you have data that has 0's as inputs without biases, that would break the model. A bias ensures the model will function regardless of the training data and allows the model to fit data that doesn't intersect the origin.
![Full Notebook](./screenshots/2.Step1.png)

### Step 2: Pass weighted sum through activation function to introduce non-linearity
The real magic of an MLP is the activation function. Without an activation function the model could be collapsed into a single equation and act more like a linear regression. For example this whole network could be collapsed into this one equation: (0.5(0.4) + 0.8(0.3) + 0.1)0.5 + (0.5(0.2) + 0.8(0.6) + 0.1)0.7 + 0.1. Instead, adding an activation function introduces non-linearity and makes it harder to collapse the network. A simple and common activation function that is used in hidden layers is ReLU which sets any negative number to 0 and retains the value of positive values. In this example I am using the Sigmoid activation function.
![Full Notebook](./screenshots/3.Step2.png)

### Step 3: Compute weighted sum for next layer
![Full Notebook](./screenshots/4.Step3.png)

### Step 4: Pass weighted sum into activation function
![Full Notebook](./screenshots/5.Step4.png)

### Step 5: Calculate Loss
![Full Notebook](./screenshots/6.Step5.png)

## Backpropagation
### Step 1: Differentiate loss function
![Full Notebook](./screenshots/7.Step1.png)

### Step 2: Differentiate the activation function
![Full Notebook](./screenshots/8.Step2.png)

### Step 3: Compute output delta (Step 1 x Step 2)
![Full Notebook](./screenshots/9.Step3.png)

### Step 4: Calculate Output Gradients
![Full Notebook](./screenshots/10.Step4.png)

### Step 5: Calculate Hidden Gradients
![Full Notebook](./screenshots/11.Step5.png)

### Step 6: Calculate Delta of the loss with respect to weight
![Full Notebook](./screenshots/12.Step6.png)

### Step 7: Update Weights
![Full Notebook](./screenshots/13.Step7.png)


## 2nd Forward Pass
### Step 1: Compute weighted sum
![Full Notebook](./screenshots/14.Step1.png)

### Step 2: Pass weighted sum through activation function to introduce non-linearity
![Full Notebook](./screenshots/15.Step2.png)

### Step 3: Compute weighted sum for next layer
![Full Notebook](./screenshots/16.Step3.png)

### Step 4: Pass weighted sum into activation function
![Full Notebook](./screenshots/17.Step4.png)

### Step 5: Calculate loss
![Full Notebook](./screenshots/18.Step5.png)

### Step 6: Calculate change in loss
![Full Notebook](./screenshots/19.Step6.png)
