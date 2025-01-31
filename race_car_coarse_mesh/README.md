* Simulation of racecar without refinement box and layers. simplefoam was used with K-Omega turbulence model.

This case was made to show the difference between the mesh refinements such as refinement boxes and boundary layers

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




