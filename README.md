# Tips  

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

#related URL  
https://jybaek.tistory.com/785  
https://blog.naver.com/PostView.nhn?isHttpsRedirect=true&blogId=rladnjsqll&logNo=221503725459&parentCategoryNo=&categoryNo=15&viewDate=&isShowPopularPosts=true&from=search
https://velog.io/@1_ne/%EC%97%90%EB%9F%ACRuntime-Error-with-DataLoader-exited-unexpectedly  
