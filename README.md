# kubeapp

**Purpose:** This repository is intended for learning purposes and serves as a playground for testing Kubernetes deployments on an AWS cluster while deploying a web application. The deployment configurations are written in YAML.

**Important Notes:**

1. **Kops Version Bug**: Be aware that there is a known bug in Kops versions greater than 1.26, where DNS zone initialization may fail. Please ensure you are using a compatible version if you encounter issues related to DNS zone initialization.

2. **Unique VolumeID**: In the `vprodbdep.yaml` file, the `volumeID` field must be unique and correspond to an AWS EBS volume. Make sure to replace `vol-xxxxxxxxxxxxx` with the actual and unique volume ID from your AWS environment.

3. **Custom Image Tagging**: Due to the absence of an "application.properties" file for the web application, it is necessary to customize the image tags in the `vproappdep.yaml` and `vprodbdep.yaml` files. Replace the following lines with the desired image tags:

   - In `vproappdep.yaml`:
     ```
     image: idodi/db:latest
     ```
   - To`vproappdep.yaml`:
     ```
     image: vprofile/vprofiledb
     ```
     
   - In `vprodbdep.yaml`:
     ```
     image: idodi/vpro:latest
     ```
   - To`vproappdep.yaml`:
     ```
     image: vprofile/vprofileapp
     ```


4. **Image Source**: It is strongly recommended to pull the required images from the "visualpath" profile on Docker Hub to ensure compatibility and to avoid potential issues related to misspellings or incorrect image sources.

Please keep these notes in mind while working with this repository to ensure a smooth deployment and learning experience. Enjoy experimenting with Kubernetes on AWS!
