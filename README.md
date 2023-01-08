# ribotv3_simulations
Simulation setup scripts and summaries of output used in the design of RiboT-v3

## What's in this repository?
We conducted folding simulations via fragment assembly using FARFAR2 in order to compare candidate tether sequences (see Figure 4 of cited paper). A premise going into these simulations was that the junction on the 23S rRNA side of the RiboT tether was not very stable (with respect to its secondary structure ensemble), since it exhibited an unusual two-way junction closed by a single GU wobble pair. Such a junction might be prone to register shifts to allow pairing with designed tether residues, frustrating our design hypothesis.

Our aim was to stabilize this junction by adding three additional closing base pairs, and then design only residues on the "16S side" of these base pairs.

We were interested in simulations that might explain why some tethers did particularly well, with the hypothesis that tethers for which the unstable two-way junction forms on its own are likely to perform better than tethers for which it instead forms a lower-energy structure.

To this end, we performed a pair of simulations for each tether. In one simulation ("constrained" in the figures), we included the unstable two-way junction in the input PDB for the folding prblem. In such simulations, there is absolutely no way for the junction to fail to form in the final fold. In the other simulations, the unstable two-way junction is not present in the input PDB. Several thousand independent trajectories were conducted for each simulation.

We then compare the score-versus-RMSD plots of the two simulations for each tether. If the unconstrained simulations form a lower-energy, higher-RMSD minimum than that achieved by the constrained simulations, then those sequences will preferentially avoid forming the two-way junction (Figure 4D). If the constrained simulations and unconstrained simulations achieve very similar minimum energies (Figure 4H), then there is no significant preference against the desired two-way junction conformation.

We conducted this simulation for four tethers from the initial "broad sampling" library and four tethers from the "designed junction" library, but summarized with one representative in Figure 4.


## Citation
Kim, D.S., et al. Three-dimensional structure-guided evolution of a ribosome with tethered subunits. Nature Chemical Biology. 2022.
