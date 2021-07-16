# voter-demo-openshift
 Voter Demo that will run on OpenShift

By default, port 80 is a privileged port in OpenShift. This breaks both the front-ends. In addition to that, the Postgres database fails to start unless you add an environment variable for the volume.