* Serial
    ```sh
    blockMesh
    surfaceFeatureExtract
    snappyHexMesh -overwrite
    icoFoam
    ```
* Parallel
    ```sh
    blockMesh
    surfaceFeatureExtract
    snappyHexMesh -overwrite
    decomposePar
    mpirun -np 4 icoFoam -parallel
    reconstructPar
    ```