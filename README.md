# tekton
gcloud artifacts repositories create sqyards --repository-format=docker \
--location=asia-south1<repo-name> --description="SqYards Docker Repo"
gcloud artifacts repositories list
gcloud auth application-default print-access-token | docker login -u oauth2accesstoken \
--password-stdin https://asia-south1-docker.pkg.dev
# tekton cli
  curl -LO https://github.com/tektoncd/cli/releases/download/v0.23.1/tektoncd-cli-0.23.1_Linux-64bit.deb
sudo dpkg -i ./tektoncd-cli-0.23.1_Linux-64bit.deb
# reference build and deploy
  https://github.com/IBM/deploy-app-using-tekton-on-kubernetes/blob/master/tekton-pipeline/task/deploy-to-cluster.yaml
