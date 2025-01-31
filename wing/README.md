* Simulation of Cessna wing with boundary layers and refinement box. simplefoam was used with laminar flow

Run the following commands to complete the grid generation and run the simulations. postprocess it to get those gifs and images at certain timesteps

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




