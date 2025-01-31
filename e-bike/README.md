* Simulation of Ebike with boundary layers and refinement box. simplefoam was used with K-Omega turbulence model

Run the following commands to complete the grid generation and run the simulations. postprocess it using ParaView to get those gifs and images at certain timesteps.
Post processing folder contains the force estimations during the simulation at the 0 folder.

```sh
foamCleanTutorials
blockMesh
surfaceFeatureExtract
snappyHexMesh -overwrite
touch a.foam
decomposePar
mpirun -np 12 simpleFoam -parallel >& log.simplefoam
reconstructPar
```




