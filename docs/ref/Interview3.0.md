**Stakeholder**: Client

**Date** : 21/03/22

**Author**: XXXX
   **Q0**: What is the problem?
   
   **A0**: We want a tool, process, methodology that helps us to model check Mealy Machines with NuSMV.

1. **Q1**: What is a MM? 
2. **A1**: A Mealy machine is a finite-state machine whose output values are determined both by its current state and the current inputs.
3. **Q2**: How is the format of a file describing a Mealy Machine? Do you have one?
4. **A2**: Well, yes I gave you an example of it and you can find an example file in the references that I gave you. See for example the file 
[MM1](MM1.png) or the one to the [MM2](https://easyexamnotes.com/p/mealy-machine.html)
6. **Q3**: What does a MM represent?
7. **A3**: Usually represent a reactive system.
8. **Q4**: What is a reactive system?
9. **A4**: Reactive systems have an ongoing interaction with their environment. MM is a formalism to model Finite State Reactive Systems. For example Hardware system, Concurrent and Distribuited Algorithm.... 
10. **Q5**: What is a SMV file?
11. **A5**: SMV stands for Symbolic Model Verifier, and it is a language that helps to model a Finite State Reactive System. You can find more infomation to the home page of [NuSMV](https://nusmv.fbk.eu/NuSMV/userman/v11/html/nusmv_2.html)
12. **Q5.1**: Why you want to use NuSMV?
13. **A5.1**: Because is one of the best model checker, faster and easy to use. Most of our researcher is skilled to use it.
14. **Q6**: Do you have any example of a smv file? 
15. **A6**: You can find more information in the link above.
16. **Q7**: Do you need a GUI to depict the MM?
17. **A7**: Well, not at the beginning. This could be a thing that can be added later on.
18. **Q8**: Which kind of applications would you like me to develop? Desktop? Web based? App?
19. **A8**: At the begininng a desktop application should be fine. May be in the future a Web based could be a good idea.
20. **Q9**: Which OS?
21. **A9**: Flexible. We prefer Linux based, then Windows and may be MacOS. Eventually a web based application could be a good thing, don'you think?
22. **Q10**: Would you like also a GUI for the SMV file? Which are the functionality of the GUI? 
23. **A10**: What do you mean?
24. **Q10.1**: Do you need a tool like notepad that allows you to modify the generated smv file before writing it on the file? 
25. **A10.1**: That's would be a nice feature, but for the moment is not relevant. 
26. **Q11**: Does the application need to interact with a database? Does there exists one?
27. **A11**: We don't need one and, no we don't have one. 
