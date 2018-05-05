# CollaSyst
Standing for Collaborative Systems, CollaSyst is an interactive and distributed system modeler/visualizer for decision-making.
A based first on Gephi (https://gephi.org) as a standalone solution, the aim is to allow online collaboration, wiki-style.

Quick links: 
* General design: https://github.com/Dfred/CoSyE/wiki/Design
* Developpers: https://github.com/Dfred/CoSyE/wiki/Contributing
* Users: https://github.com/Dfred/CoSyE/wiki/User-Documentation

# Problem
Whether humans need to handle complex abstract systems such as a governement, a computer network or a particular economy, displaying just the right amount of information is key. In effect, every individual in a group might focus on a different aspect of the system, or work at a specific level of abstraction.

Every system can be represented with directed flows (inputs or outputs) of various types, and flow transformers (functional elements/nodes) of various effect. Grouping co-functional nodes together allows collapsing their complexity into an abstract node: a node with inputs and outputs to other functional elements outside of the group.

## Use case: defining a new governmental policy
For instance, a democratic government usually consists of 3 main bodies: Executive, Legislative and Judiciary. At the highest level of abstraction, these are 3 distinct abstract nodes linked together by many flows -- money, decisions, people, etc. CollaSyst thus allows descending one level of abstraction by zooming into any of these 3 nodes until it opens-up to reveal all its constitutive nodes and internal flows. 
One could then focus on a particular aspect of the exposed internals by filtering the visualisation with masks such as "all non-people" flows.

Describing the current governmental system could be acheived through collaboration of non-experts and validating experts all of whom create nodes and their typed flows. Alledgedly non-experts would collaborate using general knowledge (basic individual tax system), whereas experts would review, fix and complete specific nodes belonging to their area of expertise.

A new governmental policy could then be formalised into a modification of the existing structure, explicitly revealing its mode of operation. A policy's effects could then be simulated by feeding the overall modified system with data representative of usual expectations (money received from taxes and given to foreign countries).

## Existing software limitations
Existing solutions such as Gephi already provide a rich set of tools for importing, editing, visualising and exploring data. However with data scientists as the target audience for this software, its interface and features represents an incredibly difficult challenge for the layman to start effectively editing or visualising the data describing the system.
Also the project aiming at realtime online collaboration, it needs to endow Gephi with addtional plugins to depart from a standalone solution.

# Proposed Solution
This project aims at skinning Gephi and developing plugins to provide the most accessible interface to non-experts.
Key objectives are providing:
* various levels of GUI simplifications so a novice user's learning curve stays optimal;
* multi-level boxes for grouping nodes (think encapsulation);
* typed links between nodes
* type-dependant (for node and/or boxes) views
* web 

