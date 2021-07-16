# voter-demo-openshift
 Voter Demo that will run on OpenShift

By default, port 80 is a privileged port in OpenShift. This breaks both the front-ends. In addition to that, the Postgres database fails to start unless you add an environment variable for the volume.

Vote is fixed by changing the app.py and Dockerfile to run Flask and Gunicorn on port 8000. Result is fixed by adding an environment variable "PORT" to the deployment file.

Once the apps run on port 8000, the Vote and Result service objects had to be updated to forward to port 8000.