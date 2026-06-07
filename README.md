# Multilayer Perceptron (from scratch)

A perceptron is a fundamental component of artificial neural networks. Inspired by the neurons in our brains*, these perceptrons make decisions and "learn" by iterating to minimize errors. When these single perceptrons are combined in layers, they form networks that can "learn" more complex patterns and make more nuanced decisions.

**Organic neurons can have different purposes, and more neurons do not necessarily mean more intelligence. I think this is really interesting because this is very similar to how artificial neurons work.*
  <br>***Fun Fact:** The African elephant brain has 257 billion neurons which is 3x the human brain. - https://pmc.ncbi.nlm.nih.gov/articles/PMC4053853/*
  
In an attempt to grasp these mechanisms more thoroughly, I decided to create my own simple multilayer perceptron and compute everything by hand (using a calculator). This process gave me a more confident and comprehensive understanding of this concept, which I can lean on when dealing with more complex systems. This process also helped to demystify AI and has given me a greater appreciation for the computing power of modern computers.

## Full Notebook
![Full Notebook](./screenshots/0.Full.png)

## Architecture
![Full Notebook](./screenshots/1.Architecture.png)

## 1st Forward Pass
### Step 1: Compute weighted sum
![Full Notebook](./screenshots/2.Step1.png)

### Step 2: Pass weighted sum through activation function to introduce non-linearity
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

![Full Notebook](./screenshots/9.Step3.png)

![Full Notebook](./screenshots/10.Step4.png)

![Full Notebook](./screenshots/11.Step5.png)

![Full Notebook](./screenshots/12.Step6.png)

![Full Notebook](./screenshots/13.Step7.png)

![Full Notebook](./screenshots/14.Step1.png)

![Full Notebook](./screenshots/15.Step2.png)

![Full Notebook](./screenshots/16.Step3.png)

![Full Notebook](./screenshots/17.Step4.png)

![Full Notebook](./screenshots/18.Step5.png)

![Full Notebook](./screenshots/19.Step6.png)
