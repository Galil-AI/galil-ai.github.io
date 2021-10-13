## GalilAI: Out-of-Task Distribution Detection using Causal Active Experimentation for Safe Transfer RL

### Abstract
Out-of-distribution (OOD) detection is a well-studied topic in supervised learning. Extending the successes in supervised learning methods to the reinforcement learning (RL) setting, however, is difficult due to the data generating process - RL agents actively query their environment for data and this data is a function of the policy followed by the agent. Thus, an agent could neglect a shift in the environment if its policy did not lead it to explore the aspect of the environment that shifted. Therefore, to achieve safe and robust generalization in RL, there exists an unmet need for OOD detection through active experimentation. Here, we attempt to bridge this lacuna by first - defining a causal framework for OOD scenarios or environments encountered by RL agents in the wild. Then, we propose a novel task - that of Out-of-Task Distribution (OOTD) detection. We introduce an RL agent which actively experiments in a test environment and subsequently concludes whether it is OOTD or not. We name our method **GalilAI**, in honor of Galileo Galilei, as it also discovers, among other causal processes, that gravitational acceleration is independent of the mass of a body. Finally, we propose a simple probabilistic neural network baseline for comparison, which extends extant Model-Based RL. We find that our method outperforms the baseline significantly. 

### Visualizations of Learned Behaviours

#### Gravitational inference whilst invariant to mass

| Normal gravitional environment | High gravitional environment |
| ------------------------------ | ---------------------------- |
| ![Normal](/data/behaviors/hopper-gravity/hopper-mass1.20-gravity-15.7-trainEnv-true-measureFall.gif) | ![High](/data/behaviors/hopper-gravity/hopper-mass1.20-gravity-15.7-testEnv-true-measureFall.gif) |
| ![Normal](/data/behaviors/cheetah-gravity/cheetah-mass1.80-gravity-15.7-trainEnv-correct-Handstand.gif)| ![High](data/behaviors/cheetah-gravity/cheetah-mass1.80-gravity-15.7-testEnv-correct-noHandstand.gif) |


_Left_: Normal gravitional environment. _Right_: High gravitational environment. 

Under **GalilAI**, agents learn to discern between high and low gravitational environments - while being invariant to their own mass - through a free-falling behavior. This action mimics Galileo's experiments that ultimately let to the experimental discovery of the [Equivalence Principle](https://en.wikipedia.org/wiki/Equivalence_principle).

#### Wind perception whilst invariant to mass
When wind was added to their environments at test-time, agents learned to use their bodies as sails as well as perform front-flips and rolls in the direction of the wind, and see how far the wind carried them along.

#### Mass detection invariant to friction
Discerning between friction (training causal factor) and agent body mass (test causal factor) is a non-trivial task, as any horizontal motions are influenced by both. **GalilAI** overcomes this, by performing handstands to test bodymass while avoiding horizontal frictional forces that may confound its judgement.

#### Perception Frequency

#### Mass - Distributional Shift in the Environment
Through light touch, agents learned an action sequence that would indeed push light blocks across their envirnment, but would not be forceful enough to push the heavy blocks around.
