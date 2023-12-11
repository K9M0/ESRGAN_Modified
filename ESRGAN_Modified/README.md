
# Environment Setup
Open anaconda prompt and cd to the folder where you have your environment.yml file
conda env create -f environment.yml
conda activate srganenv_gpu 

#### GPU
conda install pytorch==1.1.0 torchvision==0.3.0 cudatoolkit=10.0 -c pytorch

##### CPU Only
conda install pytorch-cpu==1.1.0 torchvision-cpu==0.3.0 cpuonly -c pytorch

#### TrainModel:

!python main.py --mode t --LR_path div2k_dataset/train_LR --GT_path div2k_dataset/train_HR

#### Test Model:

!python main.py --mode tsto --LR_path test_data --generator_path ./model/esrgan_custom.pt





