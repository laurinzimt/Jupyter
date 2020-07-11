Here you find some jupyter notebooks, explaining how to work with the existing local dask cluster and also a short tutorial on how to create your own conda environments. 

If you want to chose a differnt image go to /hub/home stop your server and restart it with the image of your choice

DASK
Dask.distributed is a lightweight library for distributed computing in Python, making computation in the cloud more resource efficient. If possible we recomend that you utilize this cluster to speed up your calculation tasks.

To connect to the dask-cluster use the following lines of code 

from dask.distributed import Client
c = Client('192.168.17.5:8786')
c


ENVIRONMENTS
If you want to create your own conda environments follow the following steps: 

1. copy the "environments.condarc" file to your home directory and rename it in ".condarc"


2. Create an environment, for this we will follow the example of a tensorflow environment. Open a terminal window in your Jupyter hub and use the following commands.

conda create --name tensorflow


3. Activate that environment: 

conda activate tensorflow


4. Install the wanted packages

conda install -c conda-forge tensorflow


5. Install ipykernel

conda install -c anaconda ipykernel


6. Add the environment to your jupyter notebook

python -m ipykernel install --user --name=tensorflow


Now you should see a new environment in your notebook. 
