# Configuration for FEniCS environment.
First of all, it's important to notice that by because the legacy version of FEniCS is from 2019,
by default is not compatible with any of the M1 or M2 chips, so we have to do some stuff in order 
to have a working installation.
1. First you have to have properly installed [Roseta](https://support.apple.com/en-us/HT211861)
2. Once you have that, proceed with the instalation of Conda.
3. Create a Conda environment using:
    * `conda create -n fenics`
    * `conda activate fenics`
4. Configure properly the environment, as follows:
    * `conda config --env --set subdir osx-64`
5. Proceed to install FEniCS as usual:
    * `conda install fenics`

And that's it!


# Recreating from txt source.
On the other hand, if you want to recreate your Conda environment, yu have to follow the following instructions:
1. Activate your environment 
    * `conda activate env_name`
2. Create a list of all the packages installed
    * `conda list --explicit > spec_list.txt`
3. Now, you have a .txt file with all the information for recreating your environment.
4. And, if you want to recreate it, you have to do:
    * `conda create --name ennv_name --file spec_list.txt`

And that's it!
