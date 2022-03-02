# deepOrganoid: A deep learning model to predict cellular viability in organoid cultures
Directory structure:<br />
<pre>
./datasets		Pointer to an training, growth, and testing datasets<br />
./env			Python environment for inference/deployment<br />
./Models		Pointer to external directory hosting the pre-trained deepOrganoid model exported from DLS<br />
./scripts		Scripts/code used for deploying the deepOrganoid model<br />
Run deepOrganoid	Jupyter notebook script to run the deepOrganoid models
LICENSE			Licensing infromation
README.md		This file
</pre>

# Description of the training dataset
The deepOrganoid dataset consists of 3,456 datapoints with raw brightfield images, z-project brightfield images, and biochemical "annotations" from processing the assat plates with CellTiter Glow3D after imaging. In total the dataset if from 9 patient derived colorectal organoids treated with 9 drugs in 8-point dose response with 4 technical replicates per-plate. Images were acquired on an imageXpress Microconfocal.

# Setting up the python environment
Download and install [Anaconda/Python 3.6+](https://www.anaconda.com/)<br />
Download the python envirnment yaml file in [/env](https://github.com/ReidTPowell/deepOrganoid/tree/main/env)<br />
for CPU deployments run the following command in the Anaconda prompt:<br />
	<pre>conda env create --name DLS_deployment_cpu --file env_windows_cpu.yaml</pre>
for GPU deployments run the following command in the Anaconda prompt:<br />
	<pre>conda env create --name DLS_deployment_gpu --file env_windows_gpu.yaml</pre>
After installed, activate the envirnoment using the following command:<br />
	<pre>conda env activate DLS_deployment_gpu</pre>
or activate the DLS_deployment_gpu environment using Anaconda navigator.


# Citation
RT Powell et al "deepOrganoid: A bright-field cell viability model for screening matrix embedded organoids"
