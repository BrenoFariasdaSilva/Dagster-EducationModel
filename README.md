# Dagster-EducationModel

This example is a translation of the Jupyter notebook education model to Dagster.

---

## Project Files Structure:
There are two levels of folders in this project. The first level is the project folder (root), and the second level is the Dagster folder (translated model). The project folder contains the files that are related setting up the python to a specific version (3.7.17) and dagster depencies. The Dagster folder contains the files that are related to Dagster project. Each folder level have a README.md file and a Makefile file.

## Install Dependencies:
### Pre-requisites:
First you need to run the `prerequisites.sh` file to install the project dependencies, such as `python`, `homebrew` and `node`. This file will install the `pyenv` and `pyenv-virtualenv` to manage the Python versions and virtual environments. The `homebrew` will be installed as package manager for the dagster packages. Lastly, the `node` is installed for the use of the website, in which we will have the dagster UI.

```shell
chmod +x ./prerequisites.sh # Gives execution permission to the file
./prerequisites.sh # Installs project dependencies
```

### Backend:
Now you need to run the `backend.sh` file (also located in the root directory of the project), which will create the python virtual environment and install the dagster packages, install `yarn`, the python modules and `dagit` (dagster UI).
```shell
chmod +x ./backend.sh # Gives execution permission to the file
./backend.sh # Installs project dependencies
```
Great, the dagster dependencies are installed. Now we need to install the project/model dependencies, located in `Dagster-Educacao/` folder.

### Model Dependencies:
Now that you have Python 3.7.17 installed, the Dagster dependencies and the pyenv virtual environment created, open a new terminal in the `Dagster-Educacao/` folder and execute the following makefile rule:

```shell
cd Dagster-Educacao # Enters the project folder
make dependecies # Installs the project dependencies, such as:
# Install Python dependencies of the model -> pandas, matplotlib, seaborn and scikit-learn.
# Install Docker and Docker-Compose.
# Build the docker-compose.
```
Now you have the project dependencies installed. Let's run the model.
## How to Run:
At this point, you can simply run the following command to run the model:
```shell
make dagster # Runs the model
```
This will run the dagster dev command, which will be executed on port 3000 and receive requests from any host. You can access the dagster UI by accessing the following link: http://localhost:3000.