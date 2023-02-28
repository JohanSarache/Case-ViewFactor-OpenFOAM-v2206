# Case-ViewFactor-OpenFAM-v2206
This is the OpenFoam v2206 seting of a Vacuum Radiation Test case

This case is a 2D square cavity with gray and diffuse surfaces. The case is solved transiently with the buoyantPimpleFoam solver. 

The commands to run the case are:

1) faceAgglomerate

2) viewFactorsGen

3) buoyantPimpleFoam

Optional:

In case of modifying the mesh in the "blockMeshDict" file. The "boundary" file located in "constant/polyMesh/boundary" must be modified as indicated in the OpenFoam v2206 documentation, ie.:

     floor
     {
         type            wall;
         inGroups        2(wall viewFactorWall);
         nFaces          100;
         startFace       3100;
     }

And repeat the commands:

1) faceAgglomerate

2) viewFactorsGen

3) buoyantPimpleFoam
