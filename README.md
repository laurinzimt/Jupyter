Here you will find some jupyter notebooks, explaining how to work with the existing local dask cluster. 
To connect to it use the following lines of code 

from dask.distributed import Client
c = Client('192.168.17.5:8786')
c

If you need any additional packages you can install them right in your notebook with

!pip install

But beware, at the moment these packages do not persist inbetween sessions.
