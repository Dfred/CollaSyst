# CollaSyst
Standing for Collaborative Systems, CollaSyst is an interactive and distributed system modeler/visualizer for decision-making.
Based first on Gephi (https://gephi.org) as a standalone solution, the aim is to eventually create a deployable web-based solution for real-time collaboration, wiki-style.

__Quick links:__
* Collaborative documentation: https://github.com/Dfred/CollaSyst/wiki
* General design: https://github.com/Dfred/CoSyE/wiki/Design
* Developpers: https://github.com/Dfred/CoSyE/wiki/Contributing
* Users: https://github.com/Dfred/CoSyE/wiki/User-Documentation

## Features
* graph-based knowledge management:
  * single-tag nodes and links
  * addition, edition, deletion of nodes and links
  * sequenced mutations (such as time-based animations)
  * visualisation and browsing:
    * node and link search
    * dynamic layer creation with filtering and search results
    * stackable layers
  * optional requirements:
    * source link
    * source material
* authoring
  * user registration
  * user and group management (delegation, expertise, etc.)
* traceability and validation
  * versionned modifications (diff, timestamp, etc.)
  * peer-review
* pluggable to third-party software
  * exportable data
  * optional encryption
  * optional ledger (blockchain)

# Problem
Whether humans need to handle complex abstract systems such as a governement, a computer network or a particular economy, displaying just the right amount of information is key. In effect, every individual in a group might focus on a different aspect of the system, or work at a specific level of abstraction.

Every system can be represented with directed flows (inputs or outputs) of various types, and flow transformers (functional elements/nodes) of various effect. Grouping co-functional nodes together allows collapsing their complexity into an abstract node: a node with inputs and outputs to other functional elements outside of the group.

## Use case: defining a new governmental policy
For instance, a democratic government usually consists of 3 main bodies: Executive, Legislative and Judiciary. At the highest level of abstraction, these are 3 distinct abstract nodes linked together by many flows -- money, decisions, people, etc. CollaSyst thus allows descending one level of abstraction by zooming into any of these 3 nodes until it opens-up to reveal all its constitutive nodes and internal flows. 
One could then focus on a particular aspect of the exposed internals by filtering the visualisation with masks such as "all non-people" flows.

Describing the current governmental system could be acheived through collaboration of non-experts and validating experts all of whom create nodes and their typed flows. Alledgedly non-experts would collaborate using general knowledge (for instance, basic individual tax system), whereas experts would review, fix and complete specific nodes belonging to their area of expertise.

A new governmental policy could then be formalised into a modification of the existing structure, explicitly revealing its mode of operation. A policy's effects could then be simulated by feeding the overall modified system with data representative of usual expectations (money received from taxes and given to foreign countries).

# Proposed solution

Considering parts of the above scenario can be implemented with Gephi, it sounds more reasonable to build upon Gephi until a satisfying mature version of CollaSyst emerges, and then transfer the result to the web using appropriate technologies.

## Overcoming Gephi limitations
Existing solutions such as Gephi already provide a rich set of tools for importing, editing, visualising and exploring data. However with data scientists as the target audience for this software, its interface and features represents an incredibly difficult challenge for the layman to start effectively editing or visualising the data describing the system.
Also the project aiming at realtime online collaboration, it needs to endow Gephi with addtional plugins to depart from that standalone solution.

This project can be split in two stages: 
1. adapting towards simplicity Gephi's user interface and developing plugins to provide the most accessible interface to non-experts;
1. creating a deployable server-side solution, compatible with - and visually as much similar as possible to the result of - the standalone stage.

## Roadmap
1. Standalone milestone, providing:
 * various levels of GUI simplifications so a novice user's learning curve stays optimal;
 * multi-level boxes for grouping nodes (think encapsulation);
 * tagged links between nodes (already tagged);
 * tag-dependant (for node and/or boxes) views;
 * installation scripts and/or packaging
2. Web milestone, providing:
 * a browser-based interface similar to the standalone stage;
 * trust and voting support for accepting patches;
 * standalone client communication with the server;
 * installation scripts and/or packaging.

## Relevant third-party software
CollaSyst scope should be limited to knowledge creation and visualisation, yet this is only an aspect of decision making. Thus additional tools/processes can help reach a consensus, such as debating, polling, voting, source data storage and authentication, user to individual mapping (e.g: ID validation), etc.
Here are potential candidates to plug this project with for a comprehensive solution to collaborative informed decision making:
* Decidim: https://decidim.org/features/ - a free open-source participatory democracy for cities and organizations
* 
