# GGH_24
Project Name: Optimize the NOC Design
## Brief summary :
 In order to achieve the desired performance in terms of latency, bandwidth, and buffer occupancy, the problem relates to the design of an optimal network for the ChipNOC system. The goal is to create a NOC architecture that is best suited for the intended workloads running on this system.  To achieve the optimum parameters set out in the problem statement, it is necessary to measure average latency and speed by means of an available monitor output and Reinforcement LearningRL. 
The NoC paradigm is one, if not the only one, fit to enable the integration of an exceedingly large number of computational, logic, and storage blocks in a single chip (otherwise known as a SoC). 
Our goal here is to come up with the NOC design that is best suited for target workloads running on this system.
 The optimal parameters, taking into account state, action and reward, will be determined using the RL framework. Due to their ability to deal with continuous action spaces and complex policies in high dimensional space, actor-critic based approaches such as Deep Deterministic Policy GradientDDPG or Proximal Policy OptimizationPO are recommended for this problem.
## Problem Statement :
The problem at hand is to develop the best possible Network on Chip (NOC) for a System on a Chip (SoC) that consists of a CPU and an IO peripheral that uses a weighted arbiter to access system memory.The NOC, which connects the SoC components, distributes communication between the CPU and IO peripherals to and from system memory. Each NOC component has a bi-directional connector. The goal is to come up with the NOC design that is best suited for target workloads running on this system.  On the CPU and IO interface of NOC, the traffic pattern is broken down into reads and writes. The simulator can model system memory and read response times, as well as calculate power consumption in terms of workload.  The simulator provides an overview of the CPU and IO interfaces, with a view to optimizing NOC design based on measured latency, bandwidth, buffer capacity & throttling. This solution is designed to optimize the NOC design for this SoC

## The approach used to generate the algorithm/design :
 An approach based on reinforcement learning, which is a type of machine learning that deals with decision making in complex and uncertain environments, has been used to generate an algorithm. 
Zeferion et al. presents a study that aims to estimate the switching point when NOC becomes the preferred communication architecture in Systems-on-chip.  
In order to optimize the parameters of the NOC, e.g. buffer sizes, arbitration weights and throttling frequencies according to feedback from the simulator, reinforcement learning can be used as part of the design problem for the network operations center.
 The system status is provided by the simulator, including a buffer occupancy, arbitration rate and energy consumption, as well as actions taken by the agent to adjust NOC parameters. The simulation then provides the agent with feedback in the form of measured latency, bandwidth and throttling frequency which is adapted to its policy. The complexity of the NOC design problem is a reason for using reinforcement learning in this task statement. The problem relates to continuous state and action with complex interaction between different parameters, and reinforcement learning provides a framework for optimizing the design of the NOC based on feedback from the simulator. An example of using reinforcement learning for hardware prefetching, which is a related problem in designing NOCs, can be found in the paper "Pythia: A Customizable Hardware Prefetching Framework Using Online Reinforcement Learning”.
## Proof of Correctness :
 Based on the specified requirements, this solution uses RL to improve the design parameters of the NOC. The system can learn and adapt to dynamic workload patterns, ensuring optimal performance in terms of latency, bandwidth, buffer occupancy or throttling by using an actor-critic based algorithm.
## The pseudocode to measure average latency and bandwidth using the simulator provided monitor output:
Initialize variables:
total_latency = 0
total_bandwidth = 0
total_transactions = 0
For each entry in the monitor output:
    If transaction type is a read:
        Get the timestamp of the read request
        Get the timestamp of the data response
        Calculate the latency as the difference between the response timestamp and the request timestamp
        Add the latency to the total latency variable
    If transaction type is a write:
        Get the timestamp of the write request
        Add the data size to the total bandwidth variable
    Increment the total transactions count
Calculate the average latency by dividing the total latency by the number of read transactions
Calculate the average bandwidth by dividing the total bandwidth by the number of cycles
Return the average latency and average bandwidth
 -> As this pseudocode only iterates through the monitor's output once and uses simple arithmetic operations to calculate the delay and bandwidth, it is efficient and reliable. It is also capable of handling both read and write transactions, making it applicable to a wide range of scenarios.

## Complexity Analysis :
 The complexity of the solution lies in the efficient measurement of the latency and bandwidth of the monitor's output and the training of the RL model in order to achieve optimal NOC design. The training complexity of the RL framework is dependent on the size of its state and action space, as well as convergence rates for a given algorithm.
## Alternatives considered
 Different RL algorithms such as the DQN, SARSA or ActorCritic may be used for alternative design ideas. However, in view of their suitability for continuous action spaces and complex policy learning, DDPG and PPO are preferred.
## References and appendices
Pythia: A Customizable Hardware Prefetching Framework Using Online Reinforcement Learning
Reinforcement Learning: An Introduction"
The Network-on-Chip Paradigm in Practice and Research
Network on Chip – an Overview - https://ignitarium.com/network-on-chip-an-overview/ 
Network on Chip -  https://en.wikipedia.org/wiki/Network_on_a_chip#:~:text=The%20network%20on%20chip%20is,bus%20and%20crossbar%20communication%20architectures. 


