# How does one program RGB smart contracts?

There is a big difference between the way you program RGB smart contracts and other types of blockchain-based smart-contracts \(e.g. in Ethereum\) aside from Bitcoin.  
  
In RGB there is a thing called RGB [Schema](../glossary/schema.md) which is a set of rules that define how the states of the contract can evolve in time. But unlike Ethereum or any blockchain-based smart contract  platform, you need to program the algorithm of operations.  
  
In RGB, you don't program the algorithm. Smart contract in blockchain world is an imperative \(imperatively styled\) written program, that defines a certain very restricting algorithm, which hardly can be called Turing-complete if we think of all the limitations of the underlying blockchain platforms. In RGB, we don't use imperative programming, we use a very special form of functional programming where the smart contract is defined _declaratively_. So the schema is the declarative definition of a smart contract, not imperative. So the shift of paradigm in programming RGB from programming Ethereum is the same shift of paradigm, which you need to do to move from normal imperative programming to functional programming or to declarative programming.

RGB smart contract is a direct acyclic graph \(DAG\) of the state changes, where you will always know only a portion of this graph - you don't have access to all of it. _RGB schema \(any smart contract under RGB\) is basically a set of rules of the evolution of this graph, but not in terms of operating all the graph, but applied to a single node of it and describing in a declarative manner how it can change over time._ Each of the nodes has its own rules and the resulting graph is the application of those rules. So in RGB you are not programming the way the whole graph evolves, you define how one node of the graph changes, which in turn leads to the overall evolution of the system. It's basically a cellular automata. Programming RGB smart contract is the same compared to programming [cellular automaton](https://en.wikipedia.org/wiki/Cellular_automaton). 
