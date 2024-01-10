# Conda Environment for Google Colab.


The tricky part here is to know what is the correct version that you need to install
in order to have a proper installation of HOOMD, that's the whole issue.
I'm assuming that you can use a terminal in the Colab Environment.
1. First you have to mount your Google account, this is done in the notebook via
    `from google.colab import drive`

    `drive.mount('/content/drive')`

2. Create a directory to save the miniconda installer
    `cd drive/MyDrive/`

    `mkdir src/ && cd src/`

3. Downaload the miniconda installer 
    `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

4. Install miniconda (in silent mode)
    `bash Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda`

5. Source the .bashrc
    `eval "$(/root/miniconda/bin/conda shell.bash hook)"`

6. Currently I'm using the version 2.9.6, so, in order to have that version installed you need
to create a new conda Environment to host that version
