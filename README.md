# helm101
Helm chart quickstart reference - POC steps


---
1) ```$ helm create nginx_poc ``` # create a new template file 
2) rm -rf charts  # delete charts, templates folder, notes.txt
3) Open in VSCode ; create  notes.txt;update required description 
4) create nginx_deployment.yaml and nginx_service.yaml # use this files for demo - https://github.com/Azure-Samples/azure-voting-app-redis
5) Update valyes.yaml 
    Change the port number to test  -- 
    - port: {{ .Values.service.port}} #REPLACED
 6) helm template nginx_poc #  Render chart templates locally and display the output. 
7) helm package nginx_poc/ #create the package file: something.tgz 
8) helm install mikkyapp ./nginx_poc-ssds.tgz #install the package to connected k8s/AKS from local helm client 
9) helm uninstal mikkyapp ./nginx_poc-ssds.tgz #to uninstal/cleanup 
-----------
