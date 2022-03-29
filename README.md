# Tips for docker_dnn

# Errors that may occur when installing PathPy or PyTorch  

#ModuleNotFoundError: No module named ‘fastai.vision.all’  
#ModuleNotFoundError: No module named 'IPython'  
#RuntimeError: tensor.H is only supported on matrices (2-D tensors)  

#solution  
pip install --upgrade pip  
pip install torch --upgrade   
pip install fastai --upgrade  

#related URL  
https://forums.fast.ai/t/modulenotfounderror-no-module-named-fastai-vision-all-on-kaggle-notebook/77008
https://stackoverflow.com/questions/45179915/importerror-no-module-named-ipython

# Docker SSH Connection Error  

#kex_exchange_identification: Connection closed by remote host  

#solution  
docker exec container_name service ssh restart  

#related URL   
http://shumin.co.kr/nas-docker-ssh-%EC%A0%91%EC%86%8D-error-key_exchange_identification-connection-closed-by-remote-host/    

# Docker contatiner_memory Error  

#RuntimeError: DataLoader worker (pid 985) is killed by signal: Bus error. It is possible that dataloader's workers are out of shared memory. Please try to raise your shared memory limit.  

#solution
In order to train the deep learning model in the Docker container, it is needed to reset the insufficient shared memory.
--shm-size=20G

docker run -it --shm-size=20G -v local_shared_folder:docker_shared_foler --name=container_name image_name

#related URL  
https://jybaek.tistory.com/785  

# fastai needs docker with gpu  

#solution
You can configure to access GPU resources at container startup by adding the --gpus flag.
If the ubuntu(linux) container is running and the nvidia-smi command works well, the setup is successful.

$docker run -it --shm-size=20G --gpus all -v local_shared_folder:docker_shared_foler --name=container_name image_name  
$nidiva-smi  # Find out if a GPU is available

# docker: invalid reference format: repository name must be lowercase.

#solution
Docker doesn't even allow mixed characters.

------------

https://github.com/fastai/fastbook/blob/master/01_intro.ipynb
