# PCS-usage-tutorial
### In this tutorial, we will explain three important High-performance computing resources provided by PCS such as:
1. On-demand
2. interact mode
3. Batch job.
- For more information : [Bridges-2 User Guide](https://www.psc.edu/resources/bridges-2/user-guide-2/)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
## Create an account in the bridge:
  1. Create an account in bridge xsede using your UA email
		[Signup](https://portal.xsede.org/my-xsede#/guest)
  2. Email Dr.Jiang your username to add you to our lab project
  3. Wait two business day until your account activated  
## Login to your account using the terminal:
- `ssh username@bridges2.psc.edu`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
## 1. OnDemand:
- The OnDemand interface allows you to conduct your research on Bridges-2 through a web browser. You can manage files – create, edit and move them – submit and track jobs, see job output, check the queues' status, run a Jupyter notebook through JupyterHub, and more, without logging in to Bridges-2 via traditional interfaces.
For this tutorial, we will explain launching the Jupyter notebook job, installing packages, adding datasets, etc.
  ### 1. Create conda environment
  1. First activate conda in the bridge using:
  - `module load anaconda3/2020.11`
  2. Create conda environment using the clone $AI_ENV provided with the sever:
  - `conda create --name tf2 $AI_ENV`
  3. activate the environment:
  - `source activate tf2`
  ### 2. Create customize Kernel:
  1. We need to create a Kernel to store the download packages and use it in the notebook
  - `python -m ipykernel install --user --name tf2 --display-name "Python tf"`
  ### 3. Install packages. 
  1. we can install packages using either pip or conda command
  - `pip install tensorflow`
  - `conda install tensorflow`
  ### 4. Launch Jupyter notebook 
  1. Open the link to access OnDemand [OnDemand](https://ondemand.bridges2.psc.edu/)
  2. Login using your username and password
  3. Homepage will be open 
  ![image](https://github.com/spatialdatasciencegroup/PCS-Bridge2-tutorial/blob/main/images/brige_homepage.png)
  4. Open interactive apps ad select Jupyter notebook
  ![image](https://github.com/spatialdatasciencegroup/PCS-Bridge2-tutorial/blob/main/images/interactive_apps.png)
  5. Fill the form with your job detail (Note: there are some limitation for each Partition, as you see in the GPU summary 
  ![Alt text](https://github.com/spatialdatasciencegroup/PCS-Bridge2-tutorial/blob/main/images/GPU_nodes.png?raw=true "GPU nodes")
  ![image](https://github.com/spatialdatasciencegroup/PCS-Bridge2-tutorial/blob/main/images/Launch_job.png)
  6. Launch your job and wait for a few seconds.
  ![image](https://github.com/spatialdatasciencegroup/PCS-Bridge2-tutorial/blob/main/images/Wait_accept.png)
  7. Job is ready: 
  ![image](https://github.com/spatialdatasciencegroup/PCS-Bridge2-tutorial/blob/main/images/notebook_ready.png)
  ### 5. Add dataset
  1. The bridge provides 1TB of memory to store the dataset. 
  - `/ocean/projects/ccr200015p/userName`
  2. You can use the SCP command to copy the dataset to the bridge memory using:
  - `scp file_name userName@bridges2.psc.edu:/ocean/projects/ccr200015p/userName/`

### 6. Genral information:
-  Type of GPU:
	- GPU:	
		- The GPU partition is for jobs that will use one or more entire GPU nodes.
	- GPU-shared:
		- It is for jobs that will use part of one GPU node. 
		- You can request at most 4 GPUs from one node in the GPU-shared partition.

### in progress
-------------------------------------------------------------------------------------------------------------------------------------------------------------------





