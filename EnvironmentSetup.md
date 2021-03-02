# Environment Setup Guide
This guide assumes a basic familiarity with the command line or terminal.

## The Anaconda Way (Recommended)
The easiest way to install everything needed for quantum simulation is to use Anaconda or Miniconda. The [Anaconda installation guide](https://docs.anaconda.com/anaconda/install/) should be followed for your particular operating system first.

Once Anaconda has been successfully installed, download this [environment.yml](Resources/environment.yml) file and run the command
```
conda env create -f environment.yml
```
from the directory where it was downloaded to create the `quantum_fun` environment on your system. This will install everything necessary for development with Qiskit and Cirq using Jupyter Lab. The process may take a few minutes depending on your connection speed. After Anaconda has downloaded all of the packages, you will receive a message similar to the following
```
done
#
# To activate this environment, use
#
#     $ conda activate quantum_fun
#
# To deactivate an active environment, use
#
#     $ conda deactivate
```
Next, run the command to activate the environment
```
conda activate quantum_fun
```
and then launch Jupyter Lab with the command
```
jupyter-lab
```
This should bring up a browser window pointed at http://localhost:8888/lab with shortcuts to create a Python 3 Notebook, a terminal, and several other choices.

![Empty Jupyter Lab](images/emptylab.png)

Select the Python 3 Notebook, and enter the following in the first box:
```python
import qiskit
print("Qiskit version:\n" + qiskit.__version__)

import cirq
print("\n\nCirq version:\n" + cirq.__version__ + "\n\nSample circuit:")
print(cirq.google.Foxtail)
```
Press the play button and you should receive output like the below:

![Success](images/success.png)

You're all set and ready to start developing quantum applications!

### Useful Anaconda Commands
* To deactivate the environment after use: `conda deactivate`
* To list available environments: `conda info --envs`
* To remove and environment entirely: `conda remove --name myenv --all`

For additional information, the [getting started guide](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html) is excellent, but should not be necessary for this project.

## The Individual Components Way (Advanced)
For the user who wants to customize everything and potentially read a lot of documentation in the process. This portion of the guide assumes you know what you're doing, are avoiding Anaconda for a good reason, and can work through any issues that arise while installing these components.

### Python
Check your installed version of Python from a command prompt with the command
```
python --version
```
Python 2 comes preinstalled with OS X and most Linux distributions, but Python 3 usually has to be installed separately. Follow the instructions to download and install Python for your operating system from [python.org](https://www.python.org/downloads/)

Check if Pip is installed by running
```
python -m pip --version
```
This should be the case if you downloaded the latest version of Python. Otherwise, follow the instructions at [the Pip website](https://pip.pypa.io/en/stable/installing/) to install the package manager.

### Qiskit
Install qiskit by running the command `pip install qiskit`. Verify that the install was successful by running `python -c 'import qiskit; print(qiskit.__version__)'` and verifying that it prints a version number (`0.16.4` as of March 1st, 2021) as output.

Additional installation and setup instructions can be found [here](https://qiskit.org/documentation/install.html).

### Cirq
While we don't currently plan to use Cirq, installation is equally simple with pip and just requires the command `pip install cirq`. Verify that Cirq was installed correctly by running the command `python -c 'import cirq; print(cirq.google.Foxtail)'` (may need double quotes on Windows) and verifying that it prints a circuit as output.

Additional installation and setup instructions can be found [here](https://github.com/quantumlib/Cirq/blob/master/docs/install.md) if necessary.

### Jupyter Lab
Install Jupyter Lab by running the command `pip install jupyterlab`, then verify that the install was successful by running `jupyter-lab`. A blank document should appear like this:
![Empty Jupyter Lab](images/emptylab.png)

Additional installation and setup instructions can be found [here](https://jupyter.org/install) if needed.
