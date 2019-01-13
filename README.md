## Install cloud sdk

`conda create -n python2.7 python=2.7`

`source activate python2.7`

install [google cloud sdk](https://cloud.google.com/sdk/docs/quickstart-macos#before-you-begin)

## Configure cloud project

1. **Create a new cloud project [here](https://console.cloud.google.com/cloud-resource-manager).**

   You will need a google account with a billing account. Don't worry, every new account have 300$ promotion.

2. **Enabling billing**

   If your google accout only have one account, skip it. If you have many account, select one of them for the payment of the ML-engine by referring [here](https://support.google.com/cloud/answer/6293499#enable-billing).

3. **Start ML-API**

   - Since we are using GPUs, we need to acquire the number of GPUs in [Quotas](https://console.cloud.google.com/quotas?_ga=2.186016044.-444096342.1547227127). The specific steps are as follows:

     - go to the quota page and set Metric as GPUs(all region) as ![GitHub Logo](https://www.dropbox.com/s/snfczgt8i04umjb/Screenshot%202019-01-12%2014.47.01.png?dl=0)
     - Update your account and sent the request to let your GPU number to be one.

   - Go to [Deep Learning VM](https://cloud.google.com/deep-learning-vm/docs/pytorch_start_instance) to set up the VM instance by refering PyTorch Instance with one ore more GPUs.

   - deployment Manager https://console.cloud.google.com/dm/deployments?project=testpytorch-228322

   - https://console.cloud.google.com/dm/deployments?project=testpytorch-228322

   - Create ssh connection to your machine 

     `gcloud compute ssh --project testpytorch-228322 --zone us-west1-b pytorch-1-vm -- -L 8080:localhost:8080`

   - Copy file from ML VM

     `gcloud compute scp --project testpytorch-228322 --zone us-west1-b --recurse <local file or directory> pytorch-1-vm:~/`

     

   By refering [here](https://cloud.google.com/deep-learning-vm/docs/pytorch_start_instance), select with one or more GPUs.

   

   

   

