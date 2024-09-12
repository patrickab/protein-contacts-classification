# Protein Contacts Classification

## Overview

The goal of this project is to learn to predict the tertiary structure of amino-acid contacts within proteins based on .pdf protein data.

The contact types include:

- Hydrogen bonds (HBOND)
- Van der Waals interactions (VDW)
- Disulfide bridges (SSBOND)
- Salt bridges (IONIC)
- π-π stacking (PIPISTACK)
- π-cation (PICATION)
- Metal ion coordination (METAL_ION)
- Hydrogen-halogens (HALOGEN)
- π-hydrogen bonds (PIHBOND)
- Unclassified contacts

## Custom Features

In addition to the default features, we have developed several custom features that improve the prediction accuracy of our model:

1. **Sequence-based Neighbors**: We calculate residue-level features based on neighboring residues in the sequence within a defined window. This accounts for local sequence environments that may influence the contact type.
    
2. **3D Structural Neighbors**: Using a distance-based approach, we calculate features of residues that are within a specific 3D distance cutoff (e.g., 8 Å) around each contact pair. This captures the influence of surrounding residues in the protein's 3D structure.
    
