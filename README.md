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
