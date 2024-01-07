# Configuration for FEniCS environment.
First of all, it's important to notice that by because the legacy version of FEniCS is from 2019,
by default is not compatible with any of the M1 or M2 chips, so we have to do some stuff in order 
to have a working installation.
1. First you have to have properly installed [Roseta](https://support.apple.com/en-us/HT211861)
2. Once you have that, proceed with the instalation of Conda.
3. Create a Conda environment using:
    `bash
    conda create -n fenics`
    `bash
    conda activate fenics`
4. Configure properly the environment, as follows:
    `bash
    conda config --env --set subdir osx-64`
5. Proceed to install FEniCS as usual:
    `bash
    conda install fenics`

And that's it!
