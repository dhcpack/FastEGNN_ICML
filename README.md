# Improving Equivariant Graph Neural Networks on Large Geometric Graphs via Virtual Nodes Learning

## paper
   [paper](https://www.baidu.com)

## Setup:

   ```bash
      pip -r install requirements.txt
   ```

## Run Experiments

Before executing following shell, please make sure that you specify the right `data_directory` and `log_directory` based on your machine. After the Training and Evaluating Ends, a log file will be generated in the log_directory, containing args, and losses.

**1. N-body System Dataset**

Data Generation:

```bash
   cd ./datasets/nbody/datagen
   bash run.sh
   cd ../../..
```

Train and Evaluate Model:

```bash
   bash run_nbody.sh
```

**2. Protein Molecular Dynamics Dataset**

Train and Evaluate Model:

```bash
   bash run_protein.sh
```

The Dataset will automatically download in the directory you specified.

**3. Water-3D Dataset**

Download this dataset from [link](https://springernature.figshare.com/ndownloader/files/3195389) and place it in your data dir

Train and Evaluate Model:

```bash
   bash run_simulation.sh
```

**4. QM9 Dataset**

Download this dataset from [link]()

Train and Evaluate Model:

```bash
   bash run_simulation.sh
```


## Equivariant Test

```bash
   python equivariant.py
```

It will random generate a graph `G`, rotation matrix `R` and translation vector `t`, and check `FastEGNN(G @ R + t)` equals to `FastEGNN(G) @ R + t` or not.
   


