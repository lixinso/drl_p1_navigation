[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"



### Project Overview

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.

![Trained Agent][image1]


A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

0 - move forward.
1 - move backward.
2 - turn left.
3 - turn right.
The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Algorithm


![Deep QLearning Algorithms](./imgs/Algorithm_Deep_QLearning.PNG)



### Submissions

When you are ready to submit your project, collect the following files and compress them into a single zip archive for upload:

- Navigation.ipynb
  file with fully functional code. It examine the state and action space, take random actions in the environment, train an agent using DQN and plot the scores.
  
- model.py
    It implements a regular fully connected DNN PyTorch QNetwork class. It was trained to predict the action based on the states. 
    The NeuralNetwork is used by DQN. The structure is,
    The input layer passed by the caller, followed by 2 hidden fully connected layers of 1024 cells each. The output layer decided by the caller as well.
    
- dqn_agent.py
    A DQN agent and replay buffer momory used by the DQN agent
    Agent class interacts with and learns from the environment. step() function stores the steps taken by the agent into the Replay buffer. Learn every 4 time steps. If enough samples are available in memory, get random subset and learn. act() returns actions for given state as per current policy. The learn() function update value parameters using given batch of experience tuples. The soft_update() function soft update model parameters. 
    The ReplayBuffer class is a fixed-size buffer to store experience tuples.
    
- README.md markdown file with a description of the code.

- An HTML or PDF export of the project report with the name Report.html or Report.pdf.

- A file with the saved model weights of the successful agent, can be named something like model.pt.

### DQN Settings

BUFFER_SIZE = int(1e5)  # replay buffer size
BATCH_SIZE = 64         # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR = 5e-4               # learning rate 
UPDATE_EVERY = 4        # how often to update the network

### Result

Episode 10 	 Average Score: -0.30
Episode 20 	 Average Score: -0.05
Episode 30 	 Average Score: -0.07
Episode 40 	 Average Score: 0.10
Episode 50 	 Average Score: 0.14
Episode 60 	 Average Score: 0.20
Episode 70 	 Average Score: 0.20
Episode 80 	 Average Score: 0.26
Episode 90 	 Average Score: 0.40
Episode 100 	 Average Score: 0.53
Episode 110 	 Average Score: 0.79
Episode 120 	 Average Score: 1.15
Episode 130 	 Average Score: 1.36
Episode 140 	 Average Score: 1.69
Episode 150 	 Average Score: 2.16
Episode 160 	 Average Score: 2.39
Episode 170 	 Average Score: 2.78
Episode 180 	 Average Score: 3.10
Episode 190 	 Average Score: 3.52
Episode 200 	 Average Score: 3.97
Episode 210 	 Average Score: 4.14
Episode 220 	 Average Score: 4.44
Episode 230 	 Average Score: 4.88
Episode 240 	 Average Score: 5.06
Episode 250 	 Average Score: 5.04
Episode 260 	 Average Score: 5.35
Episode 270 	 Average Score: 5.67
Episode 280 	 Average Score: 6.04
Episode 290 	 Average Score: 6.15
Episode 300 	 Average Score: 6.13
Episode 310 	 Average Score: 6.50
Episode 320 	 Average Score: 6.80
Episode 330 	 Average Score: 7.14
Episode 340 	 Average Score: 7.43
Episode 350 	 Average Score: 7.78
Episode 360 	 Average Score: 8.11
Episode 370 	 Average Score: 8.14
Episode 380 	 Average Score: 8.28
Episode 390 	 Average Score: 8.52
Episode 400 	 Average Score: 8.93
Episode 410 	 Average Score: 9.22
Episode 420 	 Average Score: 9.29
Episode 430 	 Average Score: 9.47
Episode 440 	 Average Score: 9.62
Episode 450 	 Average Score: 9.91
Episode 460 	 Average Score: 9.92
Episode 470 	 Average Score: 10.19
Episode 480 	 Average Score: 10.35
Episode 490 	 Average Score: 10.51
Episode 500 	 Average Score: 10.42
Episode 510 	 Average Score: 10.41
Episode 520 	 Average Score: 10.69
Episode 530 	 Average Score: 10.60
Episode 540 	 Average Score: 10.86
Episode 550 	 Average Score: 10.81
Episode 560 	 Average Score: 11.23
Episode 570 	 Average Score: 11.31
Episode 580 	 Average Score: 11.54
Episode 590 	 Average Score: 11.60
Episode 600 	 Average Score: 11.90
Episode 610 	 Average Score: 12.10
Episode 620 	 Average Score: 12.10
Episode 630 	 Average Score: 12.37
Episode 640 	 Average Score: 12.12
Episode 650 	 Average Score: 12.15
Episode 660 	 Average Score: 11.98
Episode 670 	 Average Score: 11.96
Episode 680 	 Average Score: 11.64
Episode 690 	 Average Score: 11.59
Episode 700 	 Average Score: 11.52
Episode 710 	 Average Score: 11.55
Episode 720 	 Average Score: 11.42
Episode 730 	 Average Score: 10.99
Episode 740 	 Average Score: 11.21
Episode 750 	 Average Score: 11.22
Episode 760 	 Average Score: 11.17
Episode 770 	 Average Score: 11.05
Episode 780 	 Average Score: 11.25
Episode 790 	 Average Score: 11.31
Episode 800 	 Average Score: 11.51
Episode 810 	 Average Score: 11.21
Episode 820 	 Average Score: 11.33
Episode 830 	 Average Score: 11.51
Episode 840 	 Average Score: 11.49
Episode 850 	 Average Score: 11.51
Episode 860 	 Average Score: 11.19
Episode 870 	 Average Score: 11.36
Episode 880 	 Average Score: 11.24
Episode 890 	 Average Score: 11.27
Episode 900 	 Average Score: 11.00
Episode 910 	 Average Score: 11.29
Episode 920 	 Average Score: 11.18
Episode 930 	 Average Score: 11.07
Episode 940 	 Average Score: 10.94
Episode 950 	 Average Score: 10.90
Episode 960 	 Average Score: 11.20
Episode 970 	 Average Score: 11.44
Episode 980 	 Average Score: 11.75
Episode 990 	 Average Score: 11.97
Episode 1000 	 Average Score: 12.04
Episode 1010 	 Average Score: 12.02
Episode 1020 	 Average Score: 12.07
Episode 1030 	 Average Score: 12.33
Episode 1040 	 Average Score: 12.49
Episode 1050 	 Average Score: 12.73
Environment solved in 958 episodes! 	 Average Score: 13.00

Total Training Time = 23.5 min


![Score](./imgs/score.png)

The result satisfied the requirement of the project: 
"A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward (over 100 episodes) of at least +13. The submission reports the number of episodes needed to solve the environment."
