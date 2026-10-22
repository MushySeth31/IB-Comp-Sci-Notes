# A4.1 — Machine Learning Fundamentals

> **How does a computer learn from data and make predictions or decisions without being explicitly programmed?**

## Machine Learning

**Machine learning (ML)** is a branch of artificial intelligence in which a computer system learns patterns from data and uses those patterns to make predictions, classifications, decisions, or discover relationships, rather than being explicitly programmed with every rule.

Machine learning is used for:

- Problems with many possible solutions
- Rules that are difficult to define explicitly
- Complex patterns
- Huge quantities of data

### Examples

- Facial recognition
- Translating languages
- Detecting spam
- Recommendation algorithms
- Detecting specific objects in images

## Traditional Programming vs Machine Learning

| Approach | Process |
|---|---|
| **Traditional programming** | Human provides rules and data → program → computer produces output |
| **Machine learning** | Data and expected outcomes/examples → training algorithm → model produces an output based on recognized patterns |

> **Traditional programming specifies the rules; machine learning learns from data.**

## The Machine Learning Process

1. Collect data
2. Prepare data
3. Train a model
4. Evaluate the model until it is good enough for deployment
5. Use the model

### Model

A **model** is a computational representation of patterns learned from data.

## Learning Approaches

The learning approaches covered in these notes are:

- Supervised learning
- Unsupervised learning
- Reinforcement learning
- Deep learning
- Transfer learning

### Supervised Learning

The model learns from **labelled training data**, where the desired output for each training example is known.

The model learns a relationship between input features and a known output, then uses that relationship to predict outputs for previously unseen data:

```text
Input features → Known output
```

#### Why Use Supervised Learning?

Supervised learning is used when data is labelled and the goal is to predict outputs for new data.

#### Supervised Learning Techniques

The two supervised-learning techniques in these notes are:

- **Classification**
- **Regression**

#### Classification

**Classification** predicts a discrete categorical output.

#### Regression

**Regression** predicts a continuous numerical output.

#### Classification vs Regression

| Dimension | Classification | Regression |
|---|---|---|
| **Output** | Category | Numerical value |
| **Output type** | Discrete | Continuous |

### Unsupervised Learning

The model receives **unlabelled data** and attempts to discover patterns, structures, relationships, or groups within it.

There is no predefined correct answer.

#### Why Use Unsupervised Learning?

Unsupervised learning is used when there is no target label to learn from.

#### Unsupervised-Learning Technique

- **Clustering**

#### Clustering

**Clustering** groups data points according to similarities.

#### Supervised vs Unsupervised Learning

| Dimension | Supervised | Unsupervised |
|---|---|---|
| **Training label** | Present | None |
| **Goal** | Predict a known output type | Discover patterns |
| **Technique** | Classification / Regression | Clustering |

### Reinforcement Learning

An **agent** learns by interacting with an environment and receiving rewards or penalties based on its actions.

#### Process

1. Observe the situation.
2. Take an action.
3. Receive a reward or penalty based on the action.
4. Learn from the reward or penalty whether to continue or avoid the action.
5. Repeat over many attempts so the system can learn which actions produce better outcomes.

### Deep Learning

**Deep learning** is based primarily on neural networks containing multiple layers, allowing the model to learn increasingly complex representations of data.

#### Structure

```text
Input → Hidden layer → Hidden layer → Output
```

Hence, the approach is called **deep**.

Deep learning is particularly useful for complex tasks such as:

- Image recognition
- Speech recognition
- Natural language processing
- Object detection

### Transfer Learning

**Transfer learning** adapts a model that has already learned useful representations from one task or dataset for another related task.

Rather than starting from zero, an existing model is fine-tuned for a new, related problem.

#### Advantages

- Less training data required
- Shorter training time
- Lower computational cost
- Can achieve good performance quickly

#### Limitations

- The model needs to be relevant enough to the new problem.
- A model trained on a certain dataset is not automatically suitable for something completely unrelated.

### Learning Approaches Summary

| Approach | Key idea |
|---|---|
| **Supervised** | Learn from labelled data |
| **Unsupervised** | Discover patterns |
| **Reinforcement** | Learn from rewards |
| **Deep learning** | Use a multi-layer neural network |
| **Transfer learning** | Reuse learned knowledge |

## Hardware Requirements in Machine Learning

Machine learning systems need to:

- Process data
- Store data
- Perform operations

Different machine-learning workloads require different hardware.

### CPU — Central Processing Unit

A **CPU** is a general-purpose processor capable of executing many different types of instructions.

Because CPUs are flexible, they are useful for:

- Sequential operations
- Development of small ML models
- General-purpose ML workloads

#### Why CPUs Aren't Always Used

Larger ML workloads require significantly more computing power and simultaneous performance.

### GPU — Graphics Processing Unit

A **GPU** is a processor designed around massive parallelism.

GPUs are useful for:

- Intensive models
- Operations that need to be performed simultaneously
- Substantially reducing training time through GPU acceleration

### TPU — Tensor Processing Unit

A **TPU** is a specialized processor designed to accelerate tensor operations used heavily in neural networks.

#### Characteristics

- Designed for machine learning
- Highly optimized for neural-network calculations
- Commonly associated with cloud-based ML infrastructure
- Less general-purpose than a CPU

#### Why Choose a TPU Over a GPU?

If a workload is heavily optimized for neural-network and tensor calculations, a TPU can provide very high efficiency.

#### Why Choose a GPU Instead?

GPUs are more general-purpose and have broader software and hardware applicability.

### FPGA — Field-Programmable Gate Array

An **FPGA** is hardware that can be configured or reconfigured after manufacturing.

#### Advantages

- Reconfigurable
- Can provide low latency
- Can be energy efficient
- Useful for specialized workloads

#### Possible Machine-Learning Applications

- Robotics
- Industrial systems
- Autonomous systems

#### Why Use an FPGA?

An FPGA is useful when a system needs specialized acceleration but its requirements may change.

### ASIC — Application-Specific Integrated Circuit

An **ASIC** is hardware designed for specific purposes.

#### Advantages

- Highly optimized
- High performance for its intended task
- Can be energy efficient

#### Limitations

- Expensive to design
- Not easily changed
- Less flexible

#### FPGA vs ASIC

| FPGA | ASIC |
|---|---|
| Configurable hardware | Purpose-built hardware |

### Edge Computing

**Edge computing** processes data near where it is generated, rather than sending everything to a central server.

```text
Sensor → Edge device → Immediate decision
```

#### Advantages

- Low latency
- Reduced bandwidth use
- Greater privacy
- Can operate offline

#### Limitations

- Limited processing power
- Low memory
- Low storage
- Low energy availability

#### Examples

- Smart cameras
- Autonomous vehicles
- Industrial sensors
- Smartphones
- Robots

### Cloud Computing

**Cloud computing** provides computational resources through remote infrastructure.

#### Advantages

- Scalable
- Flexible
- No need to maintain all physical hardware
- Suitable for large workloads

#### Limitations

- Network dependency
- Ongoing costs
- Privacy concerns
- Latency

### Edge Computing vs Cloud Computing

| Dimension | Edge computing | Cloud computing |
|---|---|---|
| **Processing location** | Near the data source | Remote infrastructure |
| **Latency** | Low | Potentially higher |
| **Data transmission** | Low data transmission | Large-scale data transmission |
| **Network requirement** | Can operate offline | Network dependent |
| **Hardware** | Limited | Highly scalable |
| **Usefulness** | Real-time decisions | Large computational workloads |

### HPC Centers — High-Performance Computing

**High-performance computing (HPC)** consists of large numbers of processors operating in parallel.

HPC centers are used for:

- Enormous datasets
- Extremely complex models
- Large simulations
- Large-scale model training

They usually contain:

- CPUs
- GPUs
- Large memory
- High-speed networks
- Massive storage

#### Examples

- Scientific research
- Weather modelling
- Genomics
- Large language models (LLMs)
- Simulations

### Hardware Summary

| Hardware | Key use |
|---|---|
| **CPU** | Small models |
| **GPU** | Neural-network training |
| **TPU** | Huge neural-network workloads |
| **FPGA** | Specialized but configurable workloads |
| **ASIC** | Highly specialized workloads |
| **HPC** | Massive computational workloads |
| **Edge** | Real-time local decisions |
| **Cloud** | Remote computing |

