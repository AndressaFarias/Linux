# Alias
alias aks-stg="kubectl config use-context stg-aks-01"

alias aks-prod="kubectl config use-context prod-aks-br-01"

alias data-stg="kubectl config use-context arn:aws:eks:us-east-1:206835565755:cluster/data-stg-eks-loggi"

alias plat-stg="kubectl config use-context arn:aws:eks:us-east-1:310090716792:cluster/platform-stg-eks-loggi"

alias plat-prod="kubectl config use-context arn:aws:eks:us-east-1:550903664601:cluster/platform-prod-eks-loggi"


-------------
alias lock='gnome-screensaver && gnome-screensaver-command --lock'

alias alert-aks-prod="kubectl config use-context prod-aks-br-01 && kubectl -n monitoring port-forward service/alertmanager-operated 9093:9093"

alias alert-eks-prod="kubectl config use-context arn:aws:eks:us-east-1:550903664601:cluster/platform-prod-eks-loggi && kubectl -n monitoring port-forward service/alertmanager-operated 9093:9093"


## Criar
    ~~~sh
        alias alias="comando"
        alias kubectl = "kubectl.exe"
    ~~~

## Mover para profile
    ~~~sh
        echo alias kubectl="kubectl.exe" >> ~/.profile
    ~~~