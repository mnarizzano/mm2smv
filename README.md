# MM2SMV CONVERTER
## From a Mealy Machine to a (Nu)SMV model 
###### On-.Going Project of Software Engineering Course at Computer Engineering Laurea(Unige) 
#### Project Description
In computer science(in particular in Artificial Intelligence), model checking is a method for checking whether a finite-state model of a system meets a given specification. In model checking we need a model of the system and a property written in some logic and a tool called model checker that checks if the model satisfy the property.

One of the most used model checker is [NuSMV](), a model checker that takes in input a finite state machine in a language called [SMV]() and a property written in [Linear Temporal Logic (LTL)](), or [Computational Tree Logic](). The model written in SMV usually define a Kripke Structure a type of  Finite State Machine. However one of the most used languages for defining Reactive Systems are the [Mealy Machines]().  So if you want to use NuSMV to model check the SMV against some LTL property you need a converter from a file representing a Mealy Machine to a SMV file. 

Goal of the project is to develop a translator from a mealy machine to a kripke structure in SMV format.

