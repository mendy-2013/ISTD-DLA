
# Introduction
This is a PyToch implementation of ISTD-DLA.  It presents a real-time industrial scene text detector, achieving the state-of-the-art performance on standard benchmarks.



## Installation

### Requirements:
- Python3
- PyTorch == 1.2 
- GCC >= 4.9 (This is important for PyTorch)
- CUDA >= 9.0 (10.1 is recommended)


```bash
  # first, make sure that your conda is setup properly with the right environment
  # for that, check that `which conda`, `which pip` and `which python` points to the
  # right path. From a clean conda env, this is what you need to do

  conda create --name ISTD-DLA -y
  conda activate ISTD-DLA

  # this installs the right pip and dependencies for the fresh python
  conda install ipython pip

  # python dependencies
  pip install -r requirement.txt

  # install PyTorch with cuda-10.1
  conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
  
  cd ISTD-DLA/

  # build deformable convolution opertor
  # make sure your cuda path of $CUDA_HOME is the same version as your cuda in PyTorch
  # make sure GCC >= 4.9
  # you need to delete the build directory before you re-build it.
  echo $CUDA_HOME
  cd assets/ops/dcn/
  python setup.py build_ext --inplace

```

### Pretrained models:
The pretrained checkpoints list in the .\backbones

### Source training && testing codes
train.py: The training function of our ISTD-DLA.

eval.py: The testing function of our ISTD-DLA.



## Datasets
The root of the dataset directory can be ```ISTD-DLA/datasets/```.




    

