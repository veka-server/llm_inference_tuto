
## Pre-requis
```
sudo apt-get update ; 
sudo apt-get upgrade -y ; 
sudo apt-get install curl wget software-properties-common python3 pip -y ; 
sudo apt-get update ;
```
## installer cuda
```
wget https://developer.download.nvidia.com/compute/cuda/12.2.2/local_installers/cuda-repo-debian11-12-2-local_12.2.2-535.104.05-1_amd64.deb;
sudo dpkg -i cuda-repo-debian11-12-2-local_12.2.2-535.104.05-1_amd64.deb;
sudo cp /var/cuda-repo-debian11-12-2-local/cuda-*-keyring.gpg /usr/share/keyrings/;
sudo add-apt-repository contrib ; 
sudo apt-get update ; 
sudo apt-get -y install cuda ;
```
## installer le serveur de LLM
```
CMAKE_ARGS="-DLLAMA_CUBLAS=on -DCMAKE_CUDA_COMPILER=/usr/local/cuda-12.2/bin/nvcc " FORCE_CMAKE=1 pip install --break-system-packages  --upgrade --force-reinstall llama-cpp-python[server] --no-cache-dir ;
```
## start serveur with model
```
export GGML_CUDA_NO_PINNED=1 && python3 -m llama_cpp.server --model /mnt/c/Users/veka/AppData/Roaming/faraday/models/openorca-platypus2-13b.Q3_K_L.gguf --n_threads=10 --host=0.0.0.0 --port=1234 --use_mlock=false --n_ctx 12000 --n_gpu_layers=43 
export GGML_CUDA_NO_PINNED=1 && python3 -m llama_cpp.server --model "/mnt/g/Ressources AI/models-llm/codellama-13b-instruct.Q3_K_L.gguf" --n_threads=10 --host=0.0.0.0 --port=1234 --use_mlock=false --n_ctx 12000 --n_gpu_layers=43 
```

