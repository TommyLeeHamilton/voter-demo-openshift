# voter-demo-openshift
 Voter Demo that will run on OpenShift

Changes to Vote: 
Modified app.py to make flask listen on port 8000 instead of 80.
New Dockerfile that starts with dockersamples/examplevotingapp_vote:before, overwrites app.py and makes entrypoint gunicorn run on port 8000.