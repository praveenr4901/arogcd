# arogcd
kubectl create ns argocd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v2.5.8/manifests/install.yaml

kubectl get all -n argocd

kubectl port-forward svc/argocd-server -n argocd 8080:443

The site will be access via localhost:443

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

use this command for finding the password

user: admin
pass:xxxxxx


