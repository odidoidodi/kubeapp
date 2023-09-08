# kubeapp
This is for learning purpose.
Some deployment tests with kubernetes cluster,AWS and  a web application.Files are written in YAML.
Please note that: There is a BUG in Kops version > 1.26 (failed to initialize DNS zones).
  To work correctly in vprodbdep.yaml file,  volumeID: vol-xxxxxxxxxxxxx  must be unique and taken from AWS's EBS.
Because of missing application.properties file of the web app, changing image: "idodi/db:latest" and "image: idodi/vpro:latest" in vproappdep.yaml and vprodbdep.yaml  is a must.Strongly sugested to change images with "vprofile/vprofiledb" and "vprofile/vprofileapp". 
