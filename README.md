## GalilAI: Out-of-Task Distribution Detection using Causal Active Experimentation for Safe Transfer RL

### Abstract
Out-of-distribution (OOD) detection is a well-studied topic in supervised learning. Extending the successes in supervised learning methods to the reinforcement learning (RL) setting, however, is difficult due to the data generating process - RL agents actively query their environment for data and this data is a function of the policy followed by the agent. Thus, an agent could neglect a shift in the environment if its policy did not lead it to explore the aspect of the environment that shifted. Therefore, to achieve safe and robust generalization in RL, there exists an unmet need for OOD detection through active experimentation. Here, we attempt to bridge this lacuna by first - defining a causal framework for OOD scenarios or environments encountered by RL agents in the wild. Then, we propose a novel task - that of Out-of-Task Distribution (OOTD) detection. We introduce an RL agent which actively experiments in a test environment and subsequently concludes whether it is OOTD or not. We name our method **GalilAI**, in honor of Galileo Galilei, as it also discovers, among other causal processes, that gravitational acceleration is independent of the mass of a body. Finally, we propose a simple probabilistic neural network baseline for comparison, which extends extant Model-Based RL. We find that our method outperforms the baseline significantly. 

### Visualizations of Learned Behaviors

#### Gravitational Experiments

<p float="middle">
  <img src="/data/behaviors/hopper-gravity/hopper-mass1.20-gravity-15.7-trainEnv-true-measureFall.gif" width="35%" title="Train env" />
  <img src="/data/behaviors/hopper-gravity/hopper-mass1.20-gravity-15.7-testEnv-true-measureFall.gif" width="35%" title="Test env" />
</p>

Under **GalilAI**, agents learn to discern between high and low gravitational environments - while being invariant to their own mass - through a free-falling behavior. This action mimics Galileo's experiments that ultimately let to the experimental discovery of the [Equivalence Principle](https://en.wikipedia.org/wiki/Equivalence_principle).

#### Wind Experiments
