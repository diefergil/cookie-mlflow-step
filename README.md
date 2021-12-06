# Cookiecutter template for MLFlow steps

Using this template you can quickly generate new steps to be used with MLFlow.

# Usage
Run the command:

```bash:
> cookiecutter [path to this repo] -o [destination directory]
```

Example:

```bash:
cookiecutter -f https://github.com/diefergil/cookie-mlflow-step.git -o src
```

configuration example:

```yaml:
step_name [step_name]: basic_cleaning
script_name [run.py]: run.py
job_type [my_step]: basic_cleaning
short_description [My step]: This steps cleans the data
long_description [An example of a step using MLflow and Weights & Biases]: Performs basic cleaning on the data and save the results in Weights & Biases
parameters [parameter1,parameter2]: parameter1,parameter2,parameter3
```

and follow the prompt. The tool will ask for the step name, the script name, the description and so on. It will
also ask for the parameters of the script. This should be a comma-separated list of parameter names *without spaces*. 
After you are done, you will find a new directory with the provided step name containing a stub of a new MLflow step.

You will need to edit both the script and the MLproject files to fill in the type and the help for the parameters.
Of course, if your script needs packages, these should be added to the conda.yml file.