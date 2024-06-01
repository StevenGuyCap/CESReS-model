# CESReS -- Code Embeddings for a Student Recommendation System
## When BERT becomes your tutor

Repository of the Master's thesis of Guillaume Steveny at UCLouvain, under the supervision of Pr. Siegfried Nijssen, Pr. Kim Mens and Julien Lienard.
The objective was to develop a machine learning model based on embeddings to classify students' submissions based on specific misconceptions.
We used GraphCodeBERT as an embedder (version from Enoch on HuggingFace) and created our training instances by developing a mutation labelling program.
This idea came from the DeepBugs [^1] system and uses Comby [^2] and RedBaron [^3] to inject the errors.

## 1. Installation

The "installation" directory contains the environment files to install the conda environments on your machine.
Select the version corresponding to your components (GPU or not).

If you have access to the CECI infrastructure, the "CECI_config.md" explains how to deploy the model on such an infrastructure.

## 2. The model program

The main program containing the model is the "cesres_graphcodebert_model.py".

Using `-h` provides explanation on command line parameters.

We designed it to work with configuration files written in Yaml.
The list of parameters lie inside the "parameters.md" file of this repository.

You can run a demo of the program with (assuming you created the conda environment):
```bash
conda activate cesres
python3 cesres_graphcodebert_model.py -c test_config.yaml
conda deactivate
# use python instead of python3 on Windows
```

## 3. The mutation labelling program

The mutation labelling program we developed for this thesis can be found inside the "mutation" directory.
Other utilities program are also available there.
Read the readme of this directory for more information.

## 3. The Graphical User Interface

The "gui" directory provides useful information to launch a GUI connecting to the Python program.
Please refer to the readme available in this directory for more information.

[^1]: https://arxiv.org/abs/1805.11683

[^2]: https://comby.dev/

[^3]: https://github.com/PyCQA/redbaron