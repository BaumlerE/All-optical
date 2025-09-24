# All-optical
Protocols for all-optical experiments 

**Basic_imaging_imports** 
- This contains a simple set of functions for loading data from suite2p

**Combinatorial_stimulation_design**
- This contains code for generating photostimulation patterns from the data (based only on x/y coordinates). 
- Here we choose a combinatorial strategy. The goal is to activate every neuron in our FOV while keeping the overall stimulation trial number low (to reduce experimental duration). To do this, we design clusters with minimal overlap in cell identify between different trials. We allow for a small degree of overlap to simplify the convergence and increase the number of neurons that can be probed for a given stimulation FOV size. Due to the off-target problem in all-optical experiments, some overlap will typicall occur regardless. One can then use reverse correlation to regress out the contirbution of individual neurons to any measured effects of stimulation. 
- This can be extended for use with functionally identified neurons (place cells, orientation tuning). 
- I recommend also extending to include an element of feature matching where needed. For example, it might be relevant to your experiment that neurons have similar baseline firing rates between the groups.  
