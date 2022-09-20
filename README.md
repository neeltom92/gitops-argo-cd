# gitops-argo-cd
setting up Argo CD for small scale organisations !

# Installation
0. Installation, Prod ready Argo CD: https://www.arthurkoziel.com/setting-up-argocd-with-helm/
1. create a common Github branch for CICD under each applications.
2. structure this branch based on Kustomise
u can refer this it for structuring it
https://betterprogramming.pub/getting-started-with-kustomize-e9a84c4c2f97
3. for external secret store u can use the operator from Godaddy.
https://medium.com/nerd-for-tech/getting-started-with-external-secrets-operator-on-kubernetes-using-aws-secrets-manager-6dc403d9630c
4. For making faster release time you have to ingrate it with Github:
https://argo-cd.readthedocs.io/en/stable/operator-manual/webhook/#:~:text=In%20your%20Git%20provider%2C%20navigate,arbitrary%20value%20in%20the%20secret.
* Ensure to create a public load balancer with limited access, only webhook IP's can be
called.

5. Slack Notifications:
* follow this :https://rinseodam.medium.com/notification-argocd-to-slack-292ce01d203b
- for additonal reference : https://github.com/argoproj-labs/argocd-notifications/issues/11
- for OAuth tokens ensure to select "bot" token
B. edit configmap and add the slacktoken under data.
