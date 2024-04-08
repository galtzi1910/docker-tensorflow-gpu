# docker-tensorflow-gpu
The simplest repo to get you started with tensorflow-gpu using docker

# Prerequisites
* You need to have an Nvidia driver installed

That's the only prerequisite, everything else should work instantly if you follow the [Getting Started](https://github.com/galtzi1910/docker-tensorflow-gpu/edit/main/README.md#getting-started) section, it's that simple!

# Getting Started
* Clone the repo
* Cd into the repo
* Run `docker-compose up` (which will build the image, it might take a few minutes)
![Screenshot_6](https://github.com/galtzi1910/docker-tensorflow-gpu/assets/97173358/0ae1dc97-e8b7-4a62-bd5e-ee5785ece72d)
* Open the url that is generated in the cmd (starts with 127.0.0.1)
![Screenshot_8](https://github.com/galtzi1910/docker-tensorflow-gpu/assets/97173358/cd54e1ad-3845-4fb7-8914-7ecab58ad44f)
* In the jupyter-lab, create a new jupyter notebook
![Screenshot_10](https://github.com/galtzi1910/docker-tensorflow-gpu/assets/97173358/706b2fc1-5454-4b1f-8303-2acc1d02d38f) 
* Add the following 2 lines to the notebook and run them:
  ```
  import tensorflow as tf
  tf.config.list_logical_devices()
  ```
  ![Screenshot_11](https://github.com/galtzi1910/docker-tensorflow-gpu/assets/97173358/818a120e-f21e-4cf9-aac8-5d4d9fb24d39)
* You will see some warnings, but if everything worked you will see the `GPU` device listed in the output (note: if you run the lines more than once, then then you won't see the warnings)
![Screenshot_12](https://github.com/galtzi1910/docker-tensorflow-gpu/assets/97173358/fa2bc281-44df-44f8-9257-43d06fa7dac3)
* If you see `LogicalDevice(name='/device:GPU:0', device_type='GPU')`, then it worked! If you only see a `CPU` device, then you are probably missing on of the [Prerequisites](https://github.com/galtzi1910/docker-tensorflow-gpu/edit/main/README.md#prerequisites)
* After that if you save the file you just created (Ctrl+S) and then kill the docker run in the cli, you should see the notebook you just created under the ./docker-tensorflow-gpu/projects directory
![Screenshot_15](https://github.com/galtzi1910/docker-tensorflow-gpu/assets/97173358/85ec3f9e-9cc7-427b-8111-da67ef0fafe3)

Now you just need to create actual projects under the `projects` folder and start training some A.Is using your GPU, good luck!
