
# CS4243 2022 Final Project

Here are the instructions for how to get this notebook up and running.


### Local Installation for OSX & Linux

* Open a Terminal and type


```sh
   # Conda installation
   curl https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -o miniconda.sh -J -L -k # Linux
   curl https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o miniconda.sh -J -L -k # OSX
   chmod +x miniconda.sh
   ./miniconda.sh
   source ~/.bashrc

   # Unzip folder

   # Install python libraries
   conda env create -f environment.yml
   source activate final_project

   # Run the notebooks in your browser
   jupyter notebook
   ```





<br><br><br><br><br><br>