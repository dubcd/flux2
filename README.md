# flux2

brew install fluxcd/tap/flux
kind create cluster 
brew install gh
gh auth login
cat ~/.config/gh/hosts.yml
export GITHUB_TOKEN=gho_

flux bootstrap github \
  --owner=anakhub \
  --repository=flux2 \
  --path=./clusters/default \
  --branch=main


# create a new blank cluster
kind create cluster

# set the token
export GITLAB_TOKEN=$(cat gitlab_token)

# re-bootstrapping Flux
flux bootstrap gitlab \
  --owner=ksn-gitops-poc \
  --repository=dev-21-jul-session \
  --path=./clusters/default \
  --branch=main
