# OpenVibSpec
![alt text](/docs/assets/img/vibspec_logo4b.png)

### Tool for an integrated analysis workflow in Vibrational Spectroscopy

Our Python library is specialised in the application of machine and deep learning (ML/DL) in the field of biospectroscopic applications. 
In recent years, most of the applications have been based on proprietary software solutions that were in the way of the FAIR principles of open science.
With strong scientific partners from the USA, England, Norway and Germany we want to pave the way for a free source code use of the common standards and latest deep learning models in biospectroscopy.  

### Contributors

- Manchester Institute of Biotechnology, The University of Manchester, (https://www.research.manchester.ac.uk/portal/en/researchers/alex-henderson(662eea20-e79b-424a-ab85-336adc2d9eb0)/contact.html)
- Biospectroscopy and Data Modeling Group, Norwegian University of Life Sciences, Ås, (https://www.nmbu.no/en/faculty/realtek/research/groups/biospectroscopy) 
- Chemical Imaging and Structures Laboratory, University of Illinois at Urbana-Champaign, (http://chemimage.illinois.edu/group.html)
- Leibniz IPHT, Jena, (https://www.leibniz-ipht.de/en/departments/photonic-data-science-2/)
- Quasar (https://quasar.codes/)
- Biomedical Analysis Group, National Academy of Sciences of Belarus, (https://image.org.by/)
### Methods and models which are included

OpenVibSpec offers the possibility to handle everything from data import of raw measurements to ML/DL based data analysis in one ecosystem. We draw on established groundwork in the Python ecosystem to guarantee the best possible longevity.

#### Infrared-based biospectroscopy of Tissue
At this point, a distinction can be made between the fields of the established ML models and the new DL models. The former is based on the model-based correction of Mie scattering. The Mie correction based worflow is based on the fundamental paradigm of making the data understandable to the individual domain experts from spectroscopy. There are several options for correcting Mie scattering, all of which we would like to introduce. But first, for an overview, see Fig.1., here we see what the workflow is based on. 

![alt text](/docs/assets/img/ir_workflow_MieCorr.png)

#### Machine Learning Models with Mie-Correction
In short:
1) After the measurement, the raw data is imported into OpenVibSpec.
2) The correction of the Mie scattering in OpenVibSpec. 
3) Selection of the training data and the training of the machine learning algorithms in OpenVibSpec (mostly Random Forest).
4) Validation of the training data and the models on independent data.


The literature on Mie-corrected data analysis in biospectroscopy, predominantly shows the use of Random Forest class classifiers after correction and selection of the training data. Currently, data can be imported into OpenVibSpec via the HDF5 and Matlab interfaces. Further, the raw data import is currently available for the Agilent FTIR and the DRS Daylight Solutions QCL spectroscopes.

#### Deep Learning Models without Mie-Correction

The second major area includes the latest methods around deep learning. Here, the immense amount of data could be used to generate models and approaches that do not require direct correction of the IR spectroscopic data. This makes the model as a whole transferable and also significantly faster to analyse. This gives us two possible workflows for segmenting DNNs in Openvibspec, as shown in Figure 2.

Option A) shows that there are FTIR spectra based on the FFPE embedding of tissue and originating from the entity colon that can be classified in this way.

Possibility B) shows the procedure e.g. for spectra from other entities or embeddings like Fresh Frozen Tissue. This results in a short transfer learning stage to make the models transferable for the own data.

![alt text](/docs/assets/img/github_workflowDL.png)


## Getting Started with OpenVibSpec
What your are reading right now is the main README. This document is in the project folder with a total of 5 other files. You can also change to three folders from here. If you would like to learn more about the installation using docker image e.g., first go to the ```documentation```folder. From this folder, you can go to the respective subfolder and read the tutorial there and paste the code copy with a mouse click to your enviroment.
```
.
├── docs
├── documentation
│   ├── Conda_Env
│   ├── DeepLearning
│   ├── Preprocessing
│   └── RawIO
├── install_packages.sh
├── MANIFEST.in
├── openvibspec_env.yml
├── README.md
├── requirements.txt
├── scr
└── setup.py
```
To copy the code snippets from the tutorials in ```documentation/..```, you only have to press the button marked in green (see screenshot below) with the mouse and the code from the selected area is already in your clipboard. But remember to change all variables after copy pasting that do not relate to the data you are using.
![alt text](/docs/assets/img/copy_paste_tutor.png)


#### References
[1](https://www.nature.com/articles/nprot.2014.110)
[2](https://onlinelibrary.wiley.com/doi/abs/10.1002/jbio.201200132)
[3](https://pubs.rsc.org/en/content/articlelanding/2010/an/b921056c/unauth)
[4](https://academic.oup.com/bioinformatics/article/36/1/287/5521621?login=true)
[5](https://onlinelibrary.wiley.com/doi/full/10.1002/jbio.202000385)
