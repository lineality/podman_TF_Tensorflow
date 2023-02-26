# podman_TF_Tensorflow


Standard Fedora TF Tensorflow Podman Steps

## 1. Podman: Get docker install links
- https://www.tensorflow.org/install 

## 2. Change docker -> podman and execute in terminal:
```
$ podman pull tensorflow/tensorflow:latest  # Download latest stable image

$ podman run -it -p 8888:8888 tensorflow/tensorflow:latest-jupyter  # Start Jupyter server
```

## 3. Open a Notebook


## 4. Upgrade pip
```
!python -m pip install --upgrade pip
```

## This is operating in a docker container, so you should not need to worry about additional layers of python venv env environments. 

## 4. Your Files Will be in a directory like this:
- /home/YOUR_NAME/.local/share/containers/storage/overlay/BIG_NUMBER/diff/tf/


## Tensorflow Example

# Podman
Podman is perhaps the next generation of docker software which runs backwards compatible with Docker. So just replace "docker" in terminal commands with "podman"

 # Run first time only: Download the latest stable image
```
$ podman pull tensorflow/tensorflow:latest 
```


## Start / Restart the jupyter notebook/labs server
```
$ podman run -it -p 8888:8888 tensorflow/tensorflow:latest-jupyter  
```

## Files will be in a path ~like this [fedora]:
#### e.g if you create a new notebook, named new_notebook.ipynb, it will be here:
```
/home/YOUR_NAME/.local/share/containers/storage/overlay/LONG#/diff/tf/new_notebook.ipynb
```

#### This should run with GPU support...details unclear (as it seems to run with GPU support without a GPU...virtual GPU container??)

...

# checking and cleaning old container files

### Check if docker is still using memory in any area:
```
$ sudo podman system df
```
### Remove Old Files (optional)
```
$ sudo podman system prune; sudo podman image prune; sudo podman volume prune; sudo podman container prune
```

