# Group Work: PanelApp Gene List Networks

## Task

1. Create a network of genes based on Hereditary spastic paraplegia panelApp.
1. Define a list of genes you would add to each panel according to network
   analysis.
1. Assess quality of sources used to create the network.
1. Prioritise list of genes according to the strength of associations within
   your network.
1. What are the major pathway *types* that are involved in your group of pathologies?
1. Discuss the strategy use to create your network.
1. Discuss the limitations of this approach.

## Process

1. Fetch:
    - List of genes from STRING.
        - Meaning of network edges: confidence.
        - Active interaction sources: experiments, databases, coexpression.
        - Minimum required interaction score: medium confidence (0.4).
        - Maximum number of interactions: <= 50 1st shell, <= 50 2nd shell.
        - Network display mode: interactive.
        - Display simplifications: hide disconnected nodes in network.
    - List of genes from PanelApp
        1. Paste into Cytoscape
        1. Add primary interactors and exclude self interactions within network (via BIOGRID plugin)

        BIOGRID is a well-defined, well-audited dataset of protein-protein interactions.
        
        Want around ~2,000 nodes in the network: too low will introduce
        sampling errors, too high will end up looking at too high a proportion
        of the human interactome, so will be computionally expensive.

1. Carry out ModuLand analysis
    - Calculate level 0 node centrality and bridgeness.
    - Calculate modules until only one most-central module remains.
    - 

1. Carry out pathway enrichment analysis from top level moduland clusters
    1. Take top 15 modules
    1. Create gene lists of top 10 central nodes in each module.
    1. Load each list into STRING-DB to find enriched KEGG and GO-BP pathways.
    1. Find most significant pathway for each module.

1. Calculate date-partyness for level 0 nodes.

## Moduland Analysis

**Moduland analyis identifies ATXN3 as the most central node.**

## Presentation

15-minute slot in scientific form.
- What is the problem?
- How has the problem been solved?
    - Present description of some of the methods.
- Results and conclusions.
- Simple table of what's been done.
- End with small executive summary.

