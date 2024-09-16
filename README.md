# synthPET
Repository for inference of our submission to the autoPETIII machine learning challenge: <br/> 
[autopet-iii.grand-challenge.org](https://autopet-iii.grand-challenge.org/autopet-iii/) 

Link to paper: [https://doi.org/10.48550/arXiv.2409.08068](https://doi.org/10.48550/arXiv.2409.08068)

## datacentric-model
This model is based on the provided 
[datacentric challenge framework](https://github.com/ClinicalDataScience/datacentric-challenge/tree/main). 
Input patches were of size (128, 160, 112), batch size was set to 4, 2 A100 GPUS were used, learning rate 1e-4 using 
SGD, trained for roughly 250k steps on all cases. During inference the model makes use of a dynamic test-time 
augmentation because of the time limit of 5 minutes. It also clips every mask values where the suv is smaller than one. 


## References
Challenge: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10990932.svg)](https://doi.org/10.5281/zenodo.10990932)<br/>
FDG Database: <a href="https://doi.org/10.7937/gkr0-xv29"><img src="https://img.shields.io/badge/DOI-10.7937%2Fgkr0--xv29-blue"></a> <br/>
PSMA Database: <a href="https://doi.org/10.7937/r7ep-3x37"><img src="https://img.shields.io/badge/DOI-10.7937%2Fr7ep--3x37-blue"></a> 





