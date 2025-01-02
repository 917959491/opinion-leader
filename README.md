

基于深度学习的意见领袖模型

Run the code
------------

#### Train model

python main.py --graph train_data --model Tripling --budget 5 --epoch 20000 --lr 0.001 --bs 16 --n_step 1

#### Test model

python main.py --graph test_data/Wiki-2.txt --model Tripling --model_file tripling.ckpt \
--budget 10 --test

python main.py --graph test_data/graph2.txt --model Tripling --model_file tripling.ckpt \
--budget 10 --test

Code files
----------

- main.py: load program arguments, graphs and set up RL agent and environment.
- runner.py: conduct simulation, train and test RL agent.
- models.py: define parameters and structures of S2V_DQN and ToupleGDD.  
- rl_agents.py: define agents to follow reinforcement learning procedure.
- environment.py: store the process of simulation.  
- utils/graph_utils.py: utility functions to load graphs, run MonteCarlo/RR to estimate influence spread.   

