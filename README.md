# User Allocation in Mobile Edge Computing: A Deep Reinforcement Learning Approach

## Installation Information

Implementation is done using conda and jupyter-notebook. 

Install Anaconda in your system. Then create a new conda environment (using environment.yml) using the following:

```bash
conda env create -f environment.yml
conda activate mecrl
```

Use `main.ipynb` to obtain the desired results.
- All the blocks except last block are function definitions.
- The last block of this Jupyter Notebook contains `for` loop which varies number of users and servers configuration.

## Project Directory Structure

- `dataset`: YOLO and MobilenetV2 execution dataset
- `dataset_generator`: Generate Dataset for training RL agent
- `eua`: EUA dataset map, Australia CBD area and codes to analyze various EUA zones
- `plots`: Various plots genereated from the .csv files are stored here
- `trained_agents`: Trained RL agents for use

## Notebooks

- `main.ipynb`: Main program to obtain allocation with different algorithms. All the algorithms are executed via function calls. The program will generate a `.csv` file. Use the .csv file to obtain plots.
- `plot_main.ipynb`: This program generates plot from `.csv` files. Allocation and agent training plots.

- `training_DDPG.ipynb`: Program to train the RL agent for various threshold using DDPG algorithm
- `training_TD3.ipynb`: Program to train the RL agent for various threshold using TD3 algorithm
- `trained_agents/edge_agent_*.zip`: DRL agent stored after training. (represented by threshold=50)

- `dataset_generator/gen_*.py`: Codes are used to generate dataset by executing YOLO and Mobilenetv2
- `eua/users.csv` and `eua/servers.csv`: Location of Usera and Servers (EUA Dataset)
- `dataset_generator/workload`: GPU workload generator used in `gen_*.py`

### Rererenced Paper:
S. P. Panda, A. Banerjee and A. Bhattacharya, "User Allocation in Mobile Edge Computing: A Deep Reinforcement Learning Approach," 2021 IEEE International Conference on Web Services (ICWS), 2021, pp. 447-458, doi: 10.1109/ICWS53863.2021.00064.
["User Allocation in Mobile Edge Computing: A Deep Reinforcement Learning Approach"](https://ieeexplore.ieee.org/document/9590334).

### Rererenced Githup Repo:
https://github.com/subratpp/mec_alloc_rl