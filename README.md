# ARGO_CD
Installation d'ArgoCD sur minikube

1.Assurez-vous que Minikube est installé sur votre Mac.

2.Démarrez Minikube en exécutant la commande minikube start.

3.Créez un espace de noms pour ArgoCD en exécutant kubectl create namespace argocd.

4.Installez ArgoCD en utilisant la commande kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml.

5.Vérifiez que les pods d'ArgoCD sont en cours d'exécution en utilisant la commande kubectl get pods -n argocd.

6.Exposez le service ArgoCD en utilisant la commande kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "NodePort"}}'.

7.Obtenez le port NodePort pour le service ArgoCD en utilisant kubectl get svc argocd-server -n argocd -o jsonpath='{.spec.ports[0].nodePort}'.

8.Obtenez l'adresse IP de Minikube en utilisant minikube ip.

9.Accédez à l'interface web d'ArgoCD en utilisant l'adresse IP de Minikube et le port NodePort précédemment obtenu.

10.Pour vous connecter, utilisez le nom d'utilisateur admin et le mot de passe généré pour ArgoCD.

Après avoir suivi ces étapes, vous devriez pouvoir utiliser ArgoCD pour déployer et gérer vos applications sur votre cluster Minikube.
