# Machine Learning-Based Ground Motion Models for Shallow Crustal Earthquakes in Active Tectonic Regions


## Table of Contents

+ [Overview](#overview)
+ [Abstract](#abstract)
+ [Install the requirements](#install)
+ [Citation](#citation)


## Overview
This folder contains the saved trained ML models on the NGA-West2 dataset. The showcase code is provided to as a sample of how to load the saved model and to create the ensemble model. Also some examples are provided to show how to plot the distance scaling and response spectra.
Since a pipeline framework has been used in Python, there is no need to process/normalize the input data for prediction and the saved models using pipeline take care of this step. The example in the showcase code is self-explanatory.

## Abstract <a name = "abstract"></a>
Data-driven ground motion models (GMMs) for the average horizontal component from shallow crustal continental earthquakes in active tectonic regions are derived using a subset of the NGA-West2 dataset including 14518 recordings out of 285 earthquakes recorded at 2347 different stations. We use four different nonparametric supervised machine learning (ML) algorithms including Artificial Neural Network, Kernel-Ridge Regressor, Random Forest Regressor, and Support Vector Regressor to construct four individual models. Then, we use a weighted average ensemble approach to combine these four models into a robust model to predict various ground motion intensity measures such as peak ground displacement (PGD), peak ground velocity (PGV), peak ground acceleration (PGA), and 5%-damped pseudo-spectral acceleration (PSA). The model input parameters are moment magnitude, rupture distance, VS30, and ZTOR. The ensemble modeling attempts to remove the drawbacks or deficiencies of different ML algorithms while capturing their advantages and also accounts for epistemic uncertainty. Although no functional form is provided, the model is able to capture salient features observed in ground motions such as saturation as well as geometrical spreading, anelastic attenuation, and nonlinear site amplification. The response spectra, as well as the magnitude, distance, VS30, and ZTOR scaling trends, are consistent and comparable with the NGA-West2 GMMs including several additional input parameters. We used a mixed-effects regression analysis to split the total aleatory uncertainty into between-event, within-station, and event-site-corrected components. The model is applicable to magnitudes from 3.0 to 8.0, rupture distances up to 300 km, and spectral periods of 0 to 10 s. 

## Install the requirements <a name = "install"></a>
* Python 3.9 and higher is required
* Create a virtual environment: conda create -n <env_name> python=3.9
* Activate the virtual environment: conda activate <env_name>
* Intall all dependencies using pip, run the command: pip install -r requirements.txt
```ShellSession
$ conda deactivate
$ conda create -n GMM python=3.9.13 anaconda
$ conda activate GMM
```
Then, install the requirements:
```ShellSession
$ pip install -r requirements.txt
```

## Citation <a name = "citation"></a>
Sedaghati, F. and S. Pezeshk, (2023). Machine Learning-Based Ground Motion Models for Shallow Crustal Earthquakes in Active Tectonic Regions, Earthquake Spectra
