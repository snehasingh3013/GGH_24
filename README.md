# GGH_24
Project Name: Optimize the NOC Design
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
## References and appendices
Pythia: A Customizable Hardware Prefetching Framework Using Online Reinforcement Learning
Reinforcement Learning: An Introduction"
The Network-on-Chip Paradigm in Practice and Research
Network on Chip – an Overview - https://ignitarium.com/network-on-chip-an-overview/ 
Network on Chip -  https://en.wikipedia.org/wiki/Network_on_a_chip#:~:text=The%20network%20on%20chip%20is,bus%20and%20crossbar%20communication%20architectures. 


