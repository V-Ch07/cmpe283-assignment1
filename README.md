# cmpe283-assignment-1

1. Firstly, Create a Google Cloud Platform Account and then Create a New Project.

2. After the Project is created, enable “Compute Engine API” for that project to create and manage Virtual Machines.

3. Once we enable Compute Engine API, Create Virtual Machine Instance using the below command. (also enable nested-virtualization)

    gcloud compute instances create instance-1 --instance1-367909 --zone=us-central1-a --machine-type=n2-standard-8 --network-interface=network-       tier=PREMIUM,subnet=default --maintenance-policy=MIGRATE --provisioning-model=STANDARD --service-account=1053649804908-compute@developer.gserviceaccount.com --           scopes=https://www.googleapis.com/auth/cloud-platform --tags=http-server,https-server --min-cpu-platform=Intel\ Cascade\ Lake --create-disk=auto-                         delete=yes,boot=yes,device-name=instance-1,image=projects/ubuntu-os-cloud/global/images/ubuntu-1804-bionic-v20221018,mode=rw,size=100,type=projects/cmpe-283-             virtualization-367909/zones/us-central1-a/diskTypes/pd-ssd --no-shielded-secure-boot --shielded-vtpm --shielded-integrity-monitoring --reservation-affinity=any --       enable-nested-virtualization
    
4. Now the instance is created. Next, open the instance by using the option "gcloud compute ssh <<instance name>>". 
  
  <img width="425" alt="image" src="https://user-images.githubusercontent.com/98682905/200491706-5fab0720-e449-4327-87c2-ae7c20720fb8.png">

5. Now, after opening an instance and getting into it, we need to clone the git repo upon modifying the "CMPE283-1.c" file. 
  
6. The CPME283-1.c file consistes of the following commands: 
    ->  Primary Process based controls (IA32_VMX_PROCBASED_CTLS).
    ->  Secondary process based controls (IA32_VMX_PROCBASED_CTLS2).
    ->  Secondary process based controls (IA32_VMX_PROCBASED_CTLS2).
    ->  Entry controls (IA32_VMX_ENTRY_CTLS).
    ->  Cannot include tertiary controls as it has Can set=No in primary controls.
  
7. Next, in the ROOt user, we need to install the required packages by using "apt install gcc (package_name)" command.
  
8. Later we need to check the version of Kernel and install the latest versions if necessary.
  
9. In order to create a kernel object, we need to execute the make command.
  
10. Then, we need to execute the sudo "insmod cmpe283-1.ko" command in order to load the kernel object.
  
11. Now, we use the "dmesg" command in order to view the output.
  
    ![1](https://user-images.githubusercontent.com/98682905/200493214-f903ec3f-0e8c-4826-b093-3f9704d6cc28.jpeg)

  
    ![2](https://user-images.githubusercontent.com/98682905/200493343-9a9b2300-be3d-4895-b996-af763381138b.jpeg)

  
    ![3](https://user-images.githubusercontent.com/98682905/200493412-c976098a-6b71-47a5-b6c7-57511ac1470a.jpeg)

  
