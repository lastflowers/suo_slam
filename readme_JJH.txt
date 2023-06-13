1. Crate virtual environment :
conda create -n cosypose python=3.7


2. Install pytorch with cuda 11.3 :
conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=11.3 -c pytorch

pytorch test
$ python3
>>> import torch
>>> torch.rand(10).to("cuda")
tensor([0.8768, 0.6031, 0.9189, 0.6784, 0.7301, 0.9469, 0.2804, 0.2625, 0.2094,
        0.7929], device='cuda:0')


3. Install dependencies
pip install -r requirements.txt 
./build_thirdparty.sh


4. run the example script
conda activate suoslam2
./eval_all_ycbv.sh
watch -n 1 nvidia-smi
sudo kill -9 <process id>