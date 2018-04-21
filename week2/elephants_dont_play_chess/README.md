# Elephants Don't Play Chess 
###### Rodney A. Brooks

## Keywords and Definitions:
1. **Situated cognition** is a theory that points out that knowing is inseparable from doing.
2. **Subsumption architecture** is based on how evolution took place. Not as complicated as humans but serves the purpose robustly. 
3. **inputs are suppressed and outputs are inhibited** ???
4. **LISP Machine** general-purpose computers designed to efficiently run Lisp as their main software and programming language, usually via hardware support.

## Introduction:
The current research in artificial intelligence seems to be saturating in terms of efficient mathematical models. Brooks argues that the reason behind this is the assumptions and methods we started off with that is the "symbolic system" or "classical AI".

Classical AI : The ML we are doing now is symbolic or general intelligence. It needs symbols as inputs where it tries to understand the symbol's architecture. Understanding the relation among various symbols is intelligence. This is how our brain works and we are trying to get that into computers. This is one way to infer intelligence.

But there seems to be another way to infer intelligence and implement the same in machines. Unlike the classical approach of modeling various components as "functional blocks" where inputs are symbols, the new or nouvelle AI models "behavioral blocks". The input is interaction with it's surroundings on various levels. This way, the performance improves as we keep adding behavioral modules. But in classical AI, the efficiency of each block needs to be increased to improve the system. But again, when blocks are increasing, we are increasing the complexity too. This is inevitable.

Brook's view is opposite of classical AI. He proves classical AI way is non-robust and difficult and a simple architecture is sufficiently sufficient. (That's not typo) 
By building a layered stack where the above layer subsumes(makes use of) below layer, it is possible to mimic a housefly completely which is better that toady's AI that models housefly's brain.

## Architecture Overview
Analogy : "Physically grounded systems" are more like the fight between heart and mind. We suddenly get an urge to do something. But then we think if doing that thing is right or not.
This was shown in the "Allen" robot and other bots too. The upper layer takes inputs from lower layers, combines it with it's own view and then it executes that action.

We are assigning numbers and symbols, ie, simulating a mathematical environment to perform operations. But the application lies completely in the real world. When the whole system is ported to real world scenario, it might not perform as expected. But the "physical grounding hypothesis" uses the inputs from real world from the beginning itself. So, at the end of training (used loosely), the system is ready to face the real world.

Debugging is not as complicated in classical AI we can easily visualize it with our eyes while it's performing. But this comes with a catch : only when every layer is near to perfect. Else, every tiny error produces another error and there'll be drastic change in output and debugging becomes difficult as the source of error is unclear by examining the output. In classical AI, though the layers are accurate, the same problem persists. Eg:DNN's layer representations which aren't human friendly.

## Verdict
This actually made a lot of sense. I always used to feel there was something missing in bringing AI into real world applications. The solution seems to be stay in the real world all the time.

But to get to the zenith of AI powered robotics, I think a mix of classical and grounded approaches are needed. And again, what proportion and other criterion depends on the use case. 

Researchers are trying to build an AI that works in any scenario and surpasses human capabilities. But we aren't even close for building an AI that does one job at 100% accuracy which a human can do. It's not that we lack the math. We might be on a wrong path that'll never make an AI system deterministic. 

So, expecting an AI to do everything at 100% definitely needs fusion of multiple approaches and methods. To achieve this complex systems, I feel efforts should be put from both these approaches and must be willing to embrace any new approaches in the future. 

It can be seen that just one cannot do everything. Hence, the title "Elephants don't play chess".
