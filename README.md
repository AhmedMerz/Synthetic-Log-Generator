# Synthetic-Log-Generator

This workflow has been developed to build suite of synthetic vertical wells.

synthetic datasets are commonly needed for method and workflow testing

this workflow is provided to support students, researchers

![image](https://github.com/user-attachments/assets/2f99e023-c0b8-4949-8a4d-714d20f8b3f7)

## Methodology
This workflow:

The data initial distribution are predefined with porosity being the primary variable for this workflow

 1) Permeability distribution is modeled on a log scale using affine transformation
 2) Resistivity distribution is modeled on a log scale using Archie law for water fully saturated rock
 3) Clay volume is an intermediate variable used to infer GR from Porosity and Shear Slowness from Compressional slowness. It is calculated using affine transformation.
 4) Density is calculated using the density log correlation for sandstone
  5) Compressional slowness is calcualted using the sonic log correlation for sandstone
 6) Shear slowness is calculated using Castagnia et al. (1985) correlation


uses GSLIB 3D simulation to build an exhaustive 3D model (regular grid) for porosity.

uses GSLIB 3D Co Simulation to build derived 3D models for all other properties assuming a certain pre-defined correlation and a secondary variable.

extracts columns of simulated values as the set of synthetic vertical well dataset

