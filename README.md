# Polynomial Efficiency and Power in Deep Networks

This project is an example testing some of the ideas presented in 
Rolnick and Tegmark's paper [The power of deeper networks for expressing natural functions](docs/RolnickTegmark.pdf),
as well as Lin, Tegmark and Rolnick's paper [Why does deep and cheap learning work so well](docs/LinTegmarkRolnick.pdf).  



### General Idea Of How It Works

The general idea is that while it has long been indicated that all nonlinear mappings can be 
accomplished with a shallow network of at least two layers, this may not be the most efficient
allocation of neurons.  The core notion comes down to the idea of factorization, and is 
expressed through a network that evaluates polynomials, which of course have quite obvious
factorization potential.  If we suppose that a network can effectively be taught to solve 
optimization problems by factoring when factoring is an option, and that factoring is a 
solution that arises from typical backpropagation, the total number of neurons can be 
dramatically reduced by having a better understanding of how the problem will be encoded 
in the network and what size network would most effectively represent solutions to the 
problem.  In general, this type of consideration helps us choose the smallest network that
achieves sufficient performance.



### Particulars Of The Implementation




### How It Is Related To Other Ideas

There is a growing interest in exploring optimal networks.  The approach of this article and
the experimentation in this project is just one mechanism.  Other interesting areas of 
exploration include using genetic algorithms to mutate parameters of the neural network and 
control the species members across generations by defining a measure of their fitness.  Matt
Harvey has been doing and shares some success in a 
[Medium post](https://medium.com/@harvitronix/lets-evolve-a-neural-network-with-a-genetic-algorithm-code-included-8809bece164) 
and his [GitHub repo](https://github.com/harvitronix/neural-network-genetic-algorithm).

All of these ideas are of great interest to me.  Ever since I started work on my 
[behavior cloning robot](https://github.com/ColinShaw/ocaml-c-behavior-cloning-robot),
which originally used a *tiny* fully connected network for control, I have been aware that 
the smallest network that is needed to solve many problems is actually fairly small.  Indeed, 
if you look at NVIDIA's [End to End Learning For Self-Driving Cars](https://arxiv.org/pdf/1604.07316v1.pdf)
paper, you may be surprised at the relatively small size of the network.  It is very 
exciting to see this new work regarding the optimization of networks using both the arbitrary
function approach as discussed by Rolnick and Tegmark, and the genetic algorithm approach as
discussed by Harvey.

