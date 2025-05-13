# RL-SMC
% The key components in this implementation are:
% 1. Actor network: directly outputs deterministic actions (control parameters)
% 2. Critic network: evaluates the value of state-action pairs (Q-values)
% 3. Target network: slowly updated versions of Actor and Critic for stable training
% 4. Experience replay buffer: stores and samples transitions (state, action, reward, next state)
% 5. Exploration noise: uses denoised Gaussian noise for action exploration
%
% Optimization process:
% 1. Generate initial action plus exploration noise using current Actor network
% 2. Execute actions and observe rewards and next states
% 3. Store experience in replay buffer
% 4. Randomly sample batches from buffer for learning
% 5. Update Critic network to minimize TD error
% 6. Update Actor network to maximize the Q-value predicted by Critic
% 7. Soft update target network
%
% Parameter tuning strategy:
% - Reduce learning rate to improve stability
% - Reduce the target network update coefficient (tau) to reduce oscillation
% - Use attenuated exploration noise to promote early exploration and later utilization
% - Design a smooth reward function to prevent gradient explosion

It is also necessary to try multiple times to determine the parameter range. Some parameters in this code have been modified and deleted. The model has been simplified.
