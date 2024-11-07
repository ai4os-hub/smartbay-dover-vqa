# smartbay-dover-vqa
[![Build Status](https://jenkins.services.ai4os.eu/buildStatus/icon?job=AI4OS-hub/smartbay-dover-vqa/main)](https://jenkins.services.ai4os.eu/job/AI4OS-hub/job/smartbay-dover-vqa/job/main/)

Implementation of DOVER VQA from ICCV 2023, Official Code for paper "Exploring Video Quality Assessment on User Generated Contents from Aesthetic and Technical Perspectives" (Wu, Haoning and Zhang, Erli and Liao, Liang and Chen, Chaofeng and Hou, Jingwen Hou and Wang, Annan and Sun, Wenxiu Sun and Yan, Qiong and Lin, Weisi)

To launch it, first install the package then run [deepaas](https://github.com/ai4os/DEEPaaS):
```bash
git clone https://github.com/ai4os-hub/smartbay-dover-vqa
cd smartbay-dover-vqa
pip install -e .
deepaas-run --listen-ip 0.0.0.0
```

## Project structure
```
│
├── Dockerfile             <- Describes main steps on integration of DEEPaaS API and
│                             smartbay_dover_vqa application in one Docker image
│
├── Jenkinsfile            <- Describes basic Jenkins CI/CD pipeline (see .sqa/)
│
├── LICENSE                <- License file
│
├── README.md              <- The top-level README for developers using this project.
│
├── VERSION                <- smartbay_dover_vqa version file
│
├── .sqa/                  <- CI/CD configuration files
│
├── smartbay_dover_vqa    <- Source code for use in this project.
│   │
│   ├── __init__.py        <- Makes smartbay_dover_vqa a Python module
│   │
│   ├── api.py             <- Main script for the integration with DEEPaaS API
│   |
│   ├── config.py          <- Configuration file to define Constants used across smartbay_dover_vqa
│   │
│   └── misc.py            <- Misc functions that were helpful accross projects
│
├── data/                  <- Folder to store the data
│
├── models/                <- Folder to store models
│   
├── tests/                 <- Scripts to perfrom code testing
|
├── metadata.json          <- Metadata information propagated to the AI4OS Hub
│
├── pyproject.toml         <- a configuration file used by packaging tools, so smartbay_dover_vqa
│                             can be imported or installed with  `pip install -e .`                             
│
├── requirements.txt       <- The requirements file for reproducing the analysis environment, i.e.
│                             contains a list of packages needed to make smartbay_dover_vqa work
│
├── requirements-test.txt  <- The requirements file for running code tests (see tests/ directory)
│
└── tox.ini                <- Configuration file for the tox tool used for testing (see .sqa/)
```
