  Upgrade the Dev Ingress Controller using the below cmd

  Validate the current helm chart version that manages the Nginx Deployment.   
  helm history  nginxinternet -n nginxinternet  

  Pre decide the chart version you want to upgrade the Nginx ingress chart to ::

  helm -n nginxinternet upgrade nginxinternet ingress-nginx/ingress-nginx --version 4.5.2 --debug
  
  --debug = This flag will showcase all the steps Helm will perform in the backend. 
  --version = This flag will hold the chart version that it will be upgraded to.
  nginxinternet = Release Name of the Helm Chart

  Steps to Validate ::

  Check the container image ID  
  kubectl describe -n nginxinternal < controller pod name >

  Ensure the service of the controller has the below parameter

  
  
  

  
