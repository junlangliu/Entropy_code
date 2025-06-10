# Entropy Changes in Water Networks Promote Protein Denaturation

The is the instruction for anyone who would like to conduct the same metadynamics simulation as used in this manuscript to explore protein folding energy landscape. (https://www.biorxiv.org/content/10.1101/2024.06.12.598657v2)

1. System requirement

   Software: NAMD 2.14 with COLVARS module

   Hardware: Cascade Lake CPU provided by Harvard FASRC. (You can run this script on any computer cluster. No requirement for non-standard hardware.)

3. Installation:

   Please refer to the following documents for the intallation of NAMD with COLVARS module: https://www.ks.uiuc.edu/Research/namd/2.14/ug/

   The installation may take 2 hours on a "normal" desktop computer

3. Demo

   Generate the initial configutations of any protein systems you want to explore or use the provided initial configurations for a single-strand alpha-helix peptide.

   Include all provided files in one folder, submit four jobs in the following order: mini.conf --> heat.conf --> equi.conf --> prod.conf

   prod.conf would generate the free energy file, which you can plot versus the collective variables to obtain the free energy landscapes as shown in this manuscript.

   The run time depends on how many steps you set for the simulations. Convergence checking is necessary if you want to obtain any reliable results. We don't suggest run this simulation on any "normal" desktop computer. With 20 CPUs, it took around 2 weeks to finish a 2-3us simulation, which are normally converged.

4. Instructions for use

   The following 4 points should be taken great care of if you are working on your own proteins.

   1) Diverse initial configurations with correct format for NAMD (Easy);
   2) Selection of collective variables (It's arts but science :) );
   3) Selection of metadynamics parameters (Depend on proteins and collective variables, much easier that point 2);
   4) Convergence check (Very important!!! Never report your results before this step. We recommend our criteria.);





