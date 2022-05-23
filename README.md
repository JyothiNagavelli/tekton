# tekton
gcloud artifacts repositories create sqyards --repository-format=docker \
--location=asia-south1<repo-name> --description="SqYards Docker Repo"
gcloud artifacts repositories list
gcloud auth application-default print-access-token | docker login -u oauth2accesstoken \
--password-stdin https://asia-south1-docker.pkg.dev
