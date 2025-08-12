# Sage Math Calculations
This project is highly used for calculator tools to inspect mathematical problems. You may try & install as follows:

## Installation
To recreate the environment from the environment.yml file in another project:

**Navigate to the project directory:**
In your terminal, change the directory to where the `environment.yml` file is located.

**Create the environment:**
Use the following command to create a new Conda environment based on the `environment.yml` file:
```shell
    conda env create -f environment.yml
```
> This will create a new environment with the same name as specified in the environment.yml file (or prompt you to name it if no name is specified in the file).

# Sagemath in Pycharm
## For Windows (using WSL):
### Install SageMath via WSL:
SageMath does not have native Windows support. Install the Windows Subsystem for Linux (WSL) and then install SageMath within your chosen Linux distribution (e.g., Ubuntu) in WSL.

### Start PyCharm from the Sage Shell (optional but recommended):
Open the WSL terminal, navigate to the directory where Sage is installed, and then open PyCharm from this terminal by typing `pycharm.sh &` **(assuming PyCharm is in your system's PATH)**. This ensures the necessary environment variables for Sage are set within PyCharm's environment.
### Configure Project Interpreter:
- Open your PyCharm project.
- Go to `File > Settings` (or `PyCharm > Preferences` on macOS).
- Navigate to `Project: [Your Project Name] > Python Interpreter`.
- Click the gear icon and select `Add Local Interpreter....`
- Choose `WSL` as the interpreter type.
- Select your WSL distribution and then browse to the path of Sage's Python executable within that WSL environment (e.g., `/usr/bin/python3` or similar, depending on your Sage installation).
- Click `OK` to add the interpreter.

## For Linux/macOS:
- **Install SageMath**: Ensure SageMath is installed on your system.
- **Start PyCharm from the Sage Shell (optional but recommended)**: Open a terminal, type `sage -sh` to enter the Sage shell, and then launch PyCharm from this shell by typing `pycharm.sh &`.
- Configure Project Interpreter:
  - Open your PyCharm project.
  - Go to `File > Settings` (or `PyCharm > Preferences` on macOS).
  - Navigate to Project: `[Your Project Name] > Python Interpreter`.
  - Click the gear icon and select `Add Local Interpreter....`
  - Choose `System Interpreter` or `Conda Environment` (if you installed Sage via Anaconda/Miniconda).
  - Browse to the path of Sage's Python executable (e.g., `/path/to/sagemath/local/bin/python`).
  - Click `OK` to add the interpreter.


# Export
## Environment
Steps to export a Conda environment:
- Activate the environment: Open your terminal or Anaconda Prompt and activate the environment you wish to export using:
```shell
    conda activate `myenv`
```
> Replace `myenv` with the actual name of your environment.

- Export the environment: Use the conda env export command to generate the environment.yml file.
```shell
    conda env export > environment.yml
```

This command exports the current environment's configuration, including all installed Conda and Pip packages and their versions, into a file named environment.yml in your current directory.
- For a more minimal export (recommended for reproducibility):
```shell
    conda env export --from-history -f environment.yml
```