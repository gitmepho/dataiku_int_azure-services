# dataiku_int_azure-services
This repo stores information on how to install Dataiku DSS on an Azure instance, integrate it with other Azure services such as Blob Storage and AKS cluster.

## Excercise 1 - Install a DSS instance (Design Node) - Install with port 11200
Given the SSH details to the Azure instance, here are the steps taken to complete excercise 1.

- SSH into the Azure VM using the username and password
- Create 2 directories for the DSS installation. INSTALL_DIR for the downloaded DSS tar.gz and DATA_DIR for the configs of Dataiku DSS (datasets, recipes, insights, models, log files, etc.)
- Change directory to the INSTALL_DIR `cd INSTALL_DIR`
- Download the DSS installer kit `wget https://downloads.dataiku.com/public/studio/12.2.3/dataiku-dss-12.2.3.tar.gz`
- Create a License file for the installation `touch dataiku-license.json` paste the provided temporary license JSON file into this file

*Check point* : Create a sample project (Dataiku TShirts) and check that you can build the flowb
