# Leak recognition
This repository is dedicated to the classification and recognition of leaks in satellite imagery

## Requirements

- Linux or macOS (Windows has not been officially tested)
- Python 3.11.x

## Installation

Step 1: Download and install Miniconda
``` bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod +x Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
```

Step 2: Clone the repository, create a conda environment, and install the requirements for the repository
``` bash
git clone https://github.com/vd-kanda/leak-recognition.git
cd leak-recognition
chmod +x create_env.sh
source create_env.sh
```

## Installation of GCS

Step 1: Install **gsutil** by following the steps described at _https://cloud.google.com/storage/docs/gsutil_inst_

Step 2: Authorize **gcloud** to access the Cloud Platform with Google user credentials
``` bash
gcloud auth login
gcloud auth application-default login
```

Step 3: Verify that DVC and GCS are properly connected and authorized
``` bash
dvc pull dvc/data/demo.dvc
```
