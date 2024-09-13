# Protein Contacts Classification

<div align="center">
    <img src="https://github.com/user-attachments/assets/d919fdd7-e0bf-46fa-8d99-b891db1572e3" alt="image" width="500">
</div>

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

### **CA-CA Distances**: Euclidean distance between the Cα atom of the source- & target residue

The CA-CA distances serve as geometric constraints that influence the protein’s 3D fold. These distances provide information on:

- Spatial proximity: Residues that are close in the folded structure will have small CA-CA distances, even if they are far apart in the sequence.
- Domain structure: By measuring CA-CA distances across the entire protein, patterns of compact folding domains and loops can be recognized.
- Secondary structure: Alpha helices and beta sheets have characteristic CA-CA distances, so such measurements can help identify where these structures are forming.

### Sequence-based Neighbors and Local Folding

Sequence-based neighbors refer to the analysis of a residue’s neighboring amino acids (left/right). We expect this feature to helps to predict local structures hence:

- Secondary structure elements: Alpha helices and beta sheets often form from specific local sequences and are stabilized by short-range interactions between adjacent or nearby residues. Its secondary structure neighbors can heavily influence the biochemical properties of a single amino acid.
- Local interactions: Proximity in sequence often leads to interactions like hydrogen bonding or hydrophobic packing, which contribute to the tertiary fold. By focusing on neighboring residues, sequence-based features can give clues about how certain regions might locally fold.

### 3D Structural Neighbors and Long-range Interactions

3D structural neighbors refer to residues that are spatially close in the protein's 3D structure but may be far apart in the primary sequence. Using a distance cutoff (e.g., 8 Å), features are derived from:

- Long-range interactions: These include contacts between residues that stabilize the protein’s overall fold (e.g., disulfide bridges, salt bridges, hydrophobic core formation).
- Folding motifs: Proteins often fold based on these long-range interactions between residues that are distant in the sequence but close in the folded structure.
- Tertiary interactions: These define how different regions of the protein interact to form the final tertiary structure. For example, a residue in one domain might interact with residues in a distant domain, forming essential tertiary contacts.

## Data Encoding/Transformation

## Feature Importance

## Management of Imbalanced Data

## Model Training

## Results
