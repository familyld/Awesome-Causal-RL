# Awesome Causal Reinforcement Learning
![Awesome](https://awesome.re/badge.svg) ![GitHub stars](https://img.shields.io/github/stars/familyld/Awesome-Causal-RL?color=yellow) ![GitHub forks](https://img.shields.io/github/forks/familyld/Awesome-Causal-RL?color=9cf) ![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg) 

The goal of this repository is to provide a curated list of resources in **Causal Reinforcement Learning (RL)**. If you have any suggestions (missing papers, tutorials, typos, or amazing blog posts), please feel free to edit and pull a request. If you find this repo helpful, please give us a star ⭐.

For people who are new to this field, we strongly recommend you to read our comprehensive survey published on TMLR (2023): [Causal Reinforcement Learning: A Survey](https://openreview.net/pdf?id=qqnttX9LPo) as a starting point. You may also find the [slides](https://2wildkids.com/talks/2023-08-21-ADMA_tutorial) of our tutorial at ADMA 2023 helpful 😉.

## Table of Contents

- [Awesome Causal Reinforcement Learning](#awesome-causal-reinforcement-learning)
  - [Table of Contents](#table-of-contents)
  - [A Brief Overview](#a-brief-overview)
  - [Talks](#talks)
  - [Papers](#papers)
    - [2023](#2023)
    - [2022](#2022)
    - [2021](#2021)
    - [2020](#2020)
    - [2019 and before](#2019-and-before)
  - [Environments](#environments)
  - [Others](#others)
  - [Contributing](#contributing)
  - [License](#license)

## A Brief Overview

![](01_Examples.png)

In practical reinforcement learning applications, understanding causality is of great significance. Take a peek at the real-life scenarios shown in the above figure:

- Imagine you're teaching a robot agent to grab things. Seems straightforward, right? But it's not just about what the robot does; it's about figureing out why certain actions can lead to the expected outcomes. If a factor changes, how does it affect the result? 
- Now, let's think about an agent trying to determine the treatment in medical scenarios. While it can access a patient's medical history, hidden factors sometimes mess things up. Maybe the socioeconomic status affects how the patients respond to treatments, and such info is missing in the records. How can the agent make the best decision under such unobserved confounders? 
- Then there's autonomous driving. To ensure safety, agents must learn from both past experiences and hypothetical scenarios where they took different actions. For instance, would a crash have occurred if the vehicle hadn't slowed down? Here, counterfactual thinking aids in safer driving.

In all these cases, causality plays a key role in decision-making, yet teaching agents to think causally is not a walk in the park. In recent years, researchers have been actively exploring systematic approaches to integrate causality into the realm of reinforcement learning, giving rise to an emerging field known as causal RL:

> Causal RL is an umbrella term for RL approaches that incorporate additional assumptions or prior knowledge to analyze and understand the causal mechanisms underlying actions and their consequences, enabling agents to make more informed and effective decisions.

This definition emphasizes two fundamental aspects that distinguish causal RL from non-causal RL. 1) It emphasizes a focus on causality, seeking to advance beyond superficial associations or data patterns. To meet this goal, 2) it necessitates the incorporation of additional assumptions or knowledge that accounts for the causal relationships inherent in decision-making problems.

## Talks

```
format:
- [title](link) [other links]
    - author1, author2, and author3...
    - conference or activity
```

- 【Tutorial】[Towards Causal Reinforcement Learning](http://auai.org/uai2019/tutorials.php#tutorial3) [[Video](https://www.youtube.com/watch?v=-cfXn3vopyw)]
  - Elias Bareinboim
  - The Conference on Uncertainty in Artificial Intelligence (UAI) 2019
- [Causal Reinforcement Learning: A Road to Artificial General Intelligence](https://www.youtube.com/watch?v=sqKcbjuXGn8) [[Slides](https://causallu.files.wordpress.com/2019/11/talkbelllabs28nov2019.pdf)]
  - Chaochao Lu
  - Social Dynamics Seminar, NOKIA Bell Labs, 28 Nov 2019
- 【Tutorial】[Towards Causal Reinforcement Learning](https://crl.causalai.net/) [[Video](https://www.youtube.com/watch?v=QRTgLWfFBMM)]
  - Elias Bareinboim
  - The International Conference on Machine Learning (ICML) 2020
- [Causal Reinforcement Learning: Motivation, Concepts, Challenges, and Applications](https://campus.swarma.org/course/2156) [[Slides](https://causallu.files.wordpress.com/2020/11/talkswarmacampus29nov2020.pdf)]
  - Chaochao Lu
  - Causal Science and Causal AI Reading Group, Swarma Campus, 29 Nov 2020
- [Towards Causal Representation Learning](https://www.youtube.com/watch?v=rKZJ0TJWvTk) [[Slides](https://www.bradyneal.com/slides/Yoshua_Bengio_Guest_Talk_Towards_Causal_Representation_Learning.pdf)]
  - Yoshua Bengio
  - Mila Causality Inference Lectures, 30 Nov 2020
- [A Survey on Causal Reinforcement Learning](https://pattern.swarma.org/study_group_issue/414) [[Paper](https://arxiv.org/pdf/2302.05209.pdf)]
  - Yan Zeng
  - Causal Science and Causal AI Reading Group, Swarma Campus, 12 Mar 2023
- 【Tutorial】[Causal Reinforcement Learning: Empowering Agents with Causality](https://adma2023.uqcloud.net/tutorial.html) [[Slides](https://2wildkids.com/talks/2023-08-21-ADMA_tutorial)]
  - Zhihong Deng, Jing Jiang
  - The International Conference on Advanced Data Mining and Applications (ADMA) 2023


## Papers

```
format:
- [title](paper link) [other links]
  - author1, author2, and author3...
  - keyword
  - code
```

### 2023
- 【Survey】[Causal Reinforcement Learning: A Survey](https://arxiv.org/abs/2307.01452)
  - Zhihong Deng, Jing Jiang, Guodong Long, Chengqi Zhang
- 【Survey】[A Survey on Causal Reinforcement Learning](https://arxiv.org/abs/2302.05209)
  - Yan Zeng, Ruichu Cai, Fuchun Sun, Libo Huang, Zhifeng Hao
- [Interpretable Reward Redistribution in Reinforcement Learning: A Causal Approach](https://openreview.net/forum?id=w7TyuWhGZP)
  - Yudi Zhang, Yali Du, Biwei Huang, Ziyan Wang, Jun Wang, Meng Fang, Mykola Pechenizkiy
  - Code: [Github Repository](https://github.com/ReedZyd/GenerativeReturnDecomposition)
- [False Correlation Reduction for Offline Reinforcement Learning](https://ieeexplore.ieee.org/document/10301548) [[Blog Post](https://familyld.github.io/posts/2023/11/SCORE/)]
  - Zhihong Deng, Zuyue Fu, Lingxiao Wang, Zhuoran Yang, Chenjia Bai, Tianyi Zhou, Zhaoran Wang, Jing Jiang
  - Code: [Github Repository](https://github.com/familyld/SCORE)
- [Learning World Models with Identifiable Factorization](https://openreview.net/forum?id=6JJq5TW9Mc)
  - Yu-Ren Liu, Biwei Huang, Zhengmao Zhu, Honglong Tian, Mingming Gong, Yang Yu, Kun Zhang
  - Code: [Github Repository](https://github.com/AlexLiuyuren/Factor)
- [Can Active Sampling Reduce Causal Confusion in Offline Reinforcement Learning?](https://proceedings.mlr.press/v213/gupta23a.html)
  - Gunshi Gupta, Tim G. J. Rudner, Rowan Thomas McAllister, Adrien Gaidon, Yarin Gal
- [Using Confounded Data in Latent Model-Based Reinforcement Learning](https://openreview.net/forum?id=nFWRuJXPkU)
  - Maxime Gasse, Damien Grasset, Guillaume Gaudron, Pierre-Yves Oudeyer
- [Delphic Offline Reinforcement Learning under Nonidentifiable Hidden Confounding](https://openreview.net/pdf?id=Jz9I_Mif7mm)
  - Alizée Pace, Hugo Yèche, Bernhard Schölkopf, Gunnar Ratsch, Guy Tennenholtz


### 2022
- 【Survey】[Causal Machine Learning: A Survey and Open Problems](https://arxiv.org/abs/2206.15475) [[Website](https://www.causal-machine-learning.com/)]
  - Jean Kaddour, Aengus Lynch, Qi Liu, Matt J. Kusner, Ricardo Silva
- [Causal Dynamics Learning for Task-Independent State Abstraction](https://proceedings.mlr.press/v162/wang22ae.html) 
  - Zizhao Wang, Xuesu Xiao, Zifan Xu, Yuke Zhu, Peter Stone
  - Code: [Github Repository](https://github.com/wangzizhao/CausalDynamicsLearning)
- [Invariant Policy Learning: A Causal Perspective](https://dl.acm.org/doi/abs/10.1109/TPAMI.2022.3232363)
  - Sorawit Saengkyongam, Nikolaj Thams, Jonas Peters,
 Niklas Pfister
  - Keyword: Causality, distributional shift, contextual bandits, off-policy learning
  - Code: [Github Repository](https://github.com/sorawitj/invariant-policy-learning)
- [Generalizing Goal-Conditioned Reinforcement Learning with Variational Causal Reasoning](https://papers.nips.cc/paper_files/paper/2022/hash/a96368eb38bce0956a1132154d70d72d-Abstract-Conference.html)
  - Wenhao Ding, Haohong Lin, Bo Li, Ding Zhao
  - Code: [Github Repository](https://github.com/GilgameshD/GRADER)
- [A Relational Intervention Approach for Unsupervised Dynamics Generalization in Model-Based Reinforcement Learning](https://openreview.net/forum?id=YRq0ZUnzKoZ)
  - Jiaxian Guo, Mingming Gong, Dacheng Tao
  - Code: [Github Repository](https://github.com/CR-Gjx/RIA)
- [MoCoDA: Model-based Counterfactual Data Augmentation](https://openreview.net/forum?id=w6tBOjPCrIO)
  - Silviu Pitis, Elliot Creager, Ajay Mandlekar, Animesh Garg
  - Code: [Github Repository](https://github.com/spitis/mocoda)
- [AdaRL: What, Where, and How to Adapt in Transfer Reinforcement Learning](https://openreview.net/forum?id=8H5bpVwvt5)
  - Biwei Huang, Fan Feng, Chaochao Lu, Sara Magliacane, Kun Zhang
  - Code: [Github Repository](https://github.com/Adaptive-RL/AdaRL-code)
- [Offline Reinforcement Learning with Causal Structured World Models](https://arxiv.org/pdf/2206.01474)
  - Zheng-Mao Zhu, Xiong-Hui Chen, Hong-Long Tian, Kun Zhang, Yang Yu
- [Provably Efficient Offline Reinforcement Learning for Partially Observable Markov Decision Processes](https://proceedings.mlr.press/v162/guo22a.html)
  - Hongyi Guo, Qi Cai, Yufeng Zhang, Zhuoran Yang, Zhaoran Wang
- [Training a Resilient Q-network against Observational Interference](https://arxiv.org/pdf/2102.09677.pdf) [[Slides](https://docs.google.com/presentation/d/1WOgnMKszZ6eYwxiR0jLZjrj7XbmKpEf9sNrbI8poSMg/edit?usp=sharing)]
  - Chao-Han Huck Yang, I-Te Danny Hung, Yi Ouyang, Pin-Yu Chen
  - Code: [Github Repository](https://github.com/huckiyang/Obs-Causal-Q-Network)
- [Online Reinforcement Learning for Mixed Policy Scopes](https://proceedings.neurips.cc/paper_files/paper/2022/hash/15349e1c554406b7719d047a498e7117-Abstract-Conference.html)
  - Junzhe Zhang, Elias Bareinboim
- [Action-Sufficient State Representation Learning for Control with Structural Constraints](https://openreview.net/forum?id=HrxfwSu8cl9)
  - Biwei Huang, Chaochao Lu, Liu Leqi, José Miguel Hernández-Lobato, Clark Glymour, Bernhard Schölkopf, Kun Zhang
- [Actual Causality and Responsibility Attribution in Decentralized Partially Observable Markov Decision Processes](https://dl.acm.org/doi/10.1145/3514094.3534133)
  - Stelios Triantafyllou, Adish Singla, Goran Radanovic
- [Reinforcement Learning of Causal Variables Using Mediation Analysis](https://ojs.aaai.org/index.php/AAAI/article/view/20648)
  - Tue Herlau, Rasmus Larsen
- [Achieving Counterfactual Fairness for Causal Bandit](https://ojs.aaai.org/index.php/AAAI/article/view/20653)
  - Wen Huang, Lu Zhang, Xintao Wu
- [SCALES: From Fairness Principles to Constrained Decision-Making](https://dl.acm.org/doi/10.1145/3514094.3534190)
  - Sreejith Balakrishnan, Jianxin Bi, Harold Soh


### 2021
- 【Survey】[Toward Causal Representation Learning](https://ieeexplore.ieee.org/abstract/document/9363924) [[Video](https://www.youtube.com/watch?v=rKZJ0TJWvTk)]
    - Bernhard Schölkopf, Francesco Locatello, Stefan Bauer, Nan Rosemary Ke, Nal Kalchbrenner, Anirudh Goyal, Yoshua Bengio
- [Invariant Causal Imitation Learning for Generalizable Policies](https://proceedings.neurips.cc/paper/2021/hash/204904e461002b28511d5880e1c36a0f-Abstract.html)
  - Ioana Bica, Daniel Jarrett, Mihaela van der Schaar
  - Code: [Github Repository](https://github.com/ioanabica/Invariant-Causal-Imitation-Learning)
- [Causal Curiosity: RL Agents Discovering Self-supervised Experiments for Causal Representation Learning](http://proceedings.mlr.press/v139/sontakke21a.html)
  - Sumedh A Sontakke, Arash Mehrjou, Laurent Itti, Bernhard Schölkopf
  - Code: [Github Repository](https://github.com/sumedh7/CausalCuriosity)
- [Causal Reasoning in Simulation for Structure and Transfer Learning of Robot Manipulation Policies](https://ieeexplore.ieee.org/document/9561439)
  - Tabitha E. Lee, Jialiang Alan Zhao, Amrita S. Sawhney, Siddharth Girdhar, Oliver Kroemer
- [CausalDyna: Improving Generalization of Dyna-style Reinforcement Learning via Counterfactual-Based Data Augmentation](https://openreview.net/pdf?id=uy602F8cTrh)
  - Deyao Zhu, Li Erran Li, Mohamed Elhoseiny
- [Learning to infer unseen contexts in causal contextual reinforcement learning](https://openreview.net/pdf?id=gPZP5ha9LpX) [[Website](https://eghbalz.github.io/carl/index.html)]
  - Hamid Eghbal-zadeh\*, Florian Henkel\*, Gerhard Widmer
  - Code: [Github Repository](https://github.com/eghbalz/contextual-gridworld)
- [Sequential Causal Imitation Learning with Unobserved Confounders](https://openreview.net/forum?id=o6-k168bBD8)
  - Daniel Kumor, Junzhe Zhang, Elias Bareinboim
- [Causal Imitation Learning under Temporally Correlated Noise](https://arxiv.org/pdf/2202.01312.pdf) [[Website](https://gokul.dev/causil/)] [[Video](https://www.youtube.com/watch?v=FPyL9vMGpFE)]
  - Gokul Swamy, Sanjiban Choudhury, J. Andrew Bagnell, Zhiwei Steven Wu
  - Code: [Github Repository](https://github.com/gkswamy98/causal_il)
- [Off-policy Evaluation in Infinite-Horizon Reinforcement Learning with Latent Confounders](http://proceedings.mlr.press/v130/bennett21a/bennett21a.pdf)
  - Andrew Bennett, Nathan Kallus, Lihong Li, Ali Mousavi
- [Provably Efficient Causal Reinforcement Learning with Confounded Observational Data](https://openreview.net/forum?id=tUeeRzMXJZ)
  - Lingxiao Wang, Zhuoran Yang, Zhaoran Wang
- [Instrumental Variable Value Iteration for Causal Offline Reinforcement Learning](https://arxiv.org/abs/2102.09907)
  - Luofeng Liao, Zuyue Fu, Zhuoran Yang, Yixin Wang, Mladen Kolar, Zhaoran Wang
- [Addressing Hindsight Bias in Multigoal Reinforcement Learning](https://ieeexplore.ieee.org/document/9531338)
  - Chenjia Bai, Lingxiao Wang, Yixin Wang, Zhaoran Wang, Rui Zhao, Chenyao Bai, Peng Liu
  - Code: [Github Repository](https://github.com/Baichenjia/BHER)
  - Keyword: Hindsight bias, hindsight experience replay (HER), reinforcement learning (RL)
- [Causal Influence Detection for Improving Efficiency in Reinforcement Learning](https://arxiv.org/abs/2106.03443)
  - Maximilian Seitzer, Bernhard Schölkopf, Georg Martius
  - Code: [Github Repository](https://github.com/martius-lab/cid-in-rl)
- [Learning "What-if" Explanations for Sequential Decision-Making](https://openreview.net/forum?id=h0de3QWtGG)
  - Ioana Bica, Daniel Jarrett, Alihan Hüyük, Mihaela van der Schaar
- [Counterfactual Credit Assignment in Model-Free Reinforcement Learning](https://proceedings.mlr.press/v139/mesnard21a.html)
  - Thomas Mesnard, Theophane Weber, Fabio Viola, Shantanu Thakoor, Alaa Saade, Anna Harutyunyan, Will Dabney, Thomas S Stepleton, Nicolas Heess, Arthur Guez, Eric Moulines, Marcus Hutter, Lars Buesing, Remi Munos
- [Counterfactual Explanations in Sequential Decision Making Under Uncertainty](https://openreview.net/forum?id=M5h1l1SldlF)
  - Stratis Tsirtsis, Abir De, Manuel Gomez Rodriguez
  - Code: [Github Repository](https://github.com/Networks-Learning/counterfactual-explanations-mdp)
- [Reward tampering problems and solutions in reinforcement learning: A causal influence diagram perspective](https://arxiv.org/abs/1908.04734)
  - Tom Everitt, Marcus Hutter, Ramana Kumar, Victoria Krakovna


### 2020
- [Invariant Causal Prediction for Block MDPs](http://proceedings.mlr.press/v119/zhang20t.html)
  - Amy Zhang, Clare Lyle, Shagun Sodhani, Angelos Filos, Marta Kwiatkowska, Joelle Pineau, Yarin Gal, Doina Precup
  - Code: [Github Repository](https://github.com/facebookresearch/icp-block-mdp)
- [Causal imitation learning with unobserved confounders](https://dl.acm.org/doi/10.5555/3495724.3496752)
  - Junzhe Zhang, Daniel Kumor, Elias Bareinboim
- [Off-policy Policy Evaluation For Sequential Decisions Under Unobserved Confounding](https://paperswithcode.com/paper/off-policy-policy-evaluation-for-sequential)
  - Hongseok Namkoong, Ramtin Keramati, Steve Yadlowsky, Emma Brunskill
  - Code: [Github Repository](https://github.com/StanfordAI4HI/off_policy_confounding)
 - [Causally Correct Partial Models for Reinforcement Learning](https://arxiv.org/abs/2002.02836)
   - Danilo J. Rezende, Ivo Danihelka, George Papamakarios, Nan Rosemary Ke, Ray Jiang, Theophane Weber, Karol Gregor, Hamza Merzic, Fabio Viola, Jane Wang, Jovana Mitrovic, Frederic Besse, Ioannis Antonoglou, Lars Buesing
- [Designing Optimal Dynamic Treatment Regimes: A Causal Reinforcement Learning Approach](https://proceedings.mlr.press/v119/zhang20a.html)
  - Junzhe Zhang, Elias Bareinboim
- [Sample-Efficient Reinforcement Learning via Counterfactual-Based Data Augmentation](https://arxiv.org/abs/2012.09092)
  - Chaochao Lu, Biwei Huang, Ke Wang, José Miguel Hernández-Lobato, Kun Zhang, Bernhard Schölkopf
- [Counterfactual Data Augmentation using Locally Factored Dynamics](https://dl.acm.org/doi/10.5555/3495724.3496059)
  - Silviu Pitis, Elliot Creager, Animesh Garg
- [Explainable Reinforcement Learning through a Causal Lens](https://ojs.aaai.org/index.php/AAAI/article/view/5631) [[Video](https://www.youtube.com/watch?v=PzzT4nRMhmM)]
  - Prashan Madumal, Tim Miller, Liz Sonenberg, Frank Vetere
- [Counterfactual Policy Evaluation for Decision-Making in Autonomous Driving](https://arxiv.org/abs/2003.11919)
  - Patrick Hart, Alois Knoll
  - Code: [Github Repository](https://github.com/bark-simulator/bark)


### 2019 and before
- [Woulda, Coulda, Shoulda: Counterfactually-Guided Policy Search](https://openreview.net/forum?id=BJG0voC9YQ)
  - Lars Buesing, Theophane Weber, Yori Zwols, Nicolas Heess, Sebastien Racaniere, Arthur Guez, Jean-Baptiste Lespiau
- [Near-Optimal Reinforcement Learning in Dynamic Treatment Regimes](https://proceedings.neurips.cc/paper/2019/hash/8252831b9fce7a49421e622c14ce0f65-Abstract.html)
  - Junzhe Zhang, Elias Bareinboim
- [Causal Induction from Visual Observations for Goal Directed Tasks](https://arxiv.org/pdf/1910.01751.pdf)
  - Suraj Nair, Yuke Zhu, Silvio Savarese, Li Fei-Fei
  - Code: [Github Repository](https://github.com/StanfordVL/causal_induction)
- [Causal Reasoning from Meta-reinforcement learning](https://openreview.net/forum?id=H1ltQ3R9KQ)
  - Ishita Dasgupta, Jane Wang, Silvia Chiappa, Jovana Mitrovic, Pedro Ortega, David Raposo, Edward Hughes, Peter Battaglia, Matthew Botvinick, Zeb Kurth-Nelson
  - Code: [Github Repository](https://github.com/threewisemonkeys-as/causal-meta-rl)
- [Counterfactual multi-agent policy gradients](https://dl.acm.org/doi/10.5555/3504035.3504398#d105486545e1) [[Video](https://www.youtube.com/watch?v=3OVvjE5B9LU)]
  - Jakob N. Foerster, Gregory Farquhar, Triantafyllos Afouras, Nantas Nardelli, Shimon Whiteson
  - Code: [Github Repository](https://github.com/matteokarldonati/Counterfactual-Multi-Agent-Policy-Gradients)
- [Fairness in Decision-Making — The Causal Explanation Formula](https://ojs.aaai.org/index.php/AAAI/article/view/11564)
  - Junzhe Zhang, Elias Bareinboim
- [Transfer Learning in Multi-Armed Bandits: A Causal Approach](https://www.ijcai.org/proceedings/2017/186)
  - Junzhe Zhang, Elias Bareinboim
  - Keyword: Knowledge Representation, Reasoning, and Logic: Action, Change and Causality; Uncertainty in AI: Graphical Models; Uncertainty in AI: Sequential Decision Making
- [Deconfounding Reinforcement Learning in Observational Settings](https://arxiv.org/abs/1812.10576)
  - Chaochao Lu, José Miguel Hernández Lobato
  - Code: [Github Repository](https://github.com/CausalRL/DRL)



## Environments
```
format:
- [name](link) [other links]
  - author1, author2, and author3...
  - description
```

- [Emei](https://github.com/FrankTianTT/emei)
  - Description: Emei is an open source Python library for developing of causal model-based reinforcement learning algorithms by providing a standard API to communicate between learning algorithms and environments, as well as a standard set of environments compliant with that API. Emei is a re-encapsulation of Openai Gym(will be replaced by Gymnasium soon).
- [CausalMBRL](https://github.com/dido1998/CausalMBRL#chemistry-environment)
  - Nan Rosemary Ke, Aniket Didolkar, Sarthak Mittal, Anirudh Goyal, Guillaume Lajoie, Stefan Bauer, Danilo Rezende, Yoshua Bengio, Michael Mozer, Christopher Pal
  - Description: The CausalMBRL dataset is created to test the causal learning abilities of model-based reinforcement learning agents. It contains 2 environments: The Physics Environment and The Chemistry Environment. Both the environments consist of blocks of various colors, shapes, and weights placed in a grid. For both the environments,there exists a ground-truth causal graph which dictates how the blocks interact. This graph is unknown to the model and should be discovered by it through interactions with the environment.
- [CausalWorld](https://github.com/rr-learning/CausalWorld) [[Website](https://sites.google.com/view/causal-world/home)]
  - CausalWorld is an open-source simulation framework and benchmark for causal structure and transfer learning in a robotic manipulation environment (powered by bullet) where tasks range from rather simple to extremely hard. Tasks consist of constructing 3D shapes from a given set of blocks - inspired by how children learn to build complex structures. 
- [Contextual Grid-world](https://github.com/eghbalz/contextual-gridworld)
  - Hamid Eghbal-zadeh\*, Florian Henkel\* and Gerhard Widmer
  - Description: Agents are trained on a set of training contexts, and are evaluated on two different sets of testing contexts. The aim is to evaluate how well agents captured the causal variables from the training, and can reason to correctly infer and generalise to new (test) contexts.


## Others

- [Blog] [因果科学 x Agents | TMLR (2023) 因果强化学习最新综述](https://zhuanlan.zhihu.com/p/668830312): A Chinese blog post about our survey on causal reinforcement learning, and its English version is HERE: [Causality x Agents: TMLR (2023) The Latest Survey on Causal Reinforcement Learning](https://2wildkids.com/posts/2023/12/CausalRL/). Eager to explore the field quickly? This blog is for you!
- [Project] [Causal-MBRL](https://github.com/polixir/causal-mbrl): a toolbox for facilitating the development of Causal Model-based Reinforcement learning algorithms.
- [Blog] [Introduction to Causal RL by Chaochao Lu](https://causallu.com/2018/12/31/introduction-to-causalrl/): a blog post about how causal reinforcement learning can improve healthcare and medicine by using causal reinforcement learning to learn from fewer data, adapt to changing environments, and handle confounding factors.
- [Blog] [Causal Reinforcement Learning: A Primer](https://stjohngrimbly.com/causal-reinforcement-learning/): A blog series that introduces and explains Elias Bareinboim’s tutorial on Causal RL at ICML 2020.  


## Contributing

If you are interested in contributing, please refer to [HERE](CONTRIBUTING.md) for instructions in contribution.


## License

This project is released under the Apache 2.0 license.



