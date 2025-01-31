# Steps

1. Compile solver
    * ```sh
      cd simpleConvectionSolver
      wmake
      ```
2. Run test case
    * ```sh
      cd case_1D_simple_convection
      blockMesh
      setFields
      simpleConvection
      ```