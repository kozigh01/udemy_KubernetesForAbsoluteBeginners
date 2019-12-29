# Udemy: Kubernetes for the Absolute Beginner

## Resources

* Course: [udemy](https://www.udemy.com/course/learn-kubernetes/)
* Code: [github](https://github.com/kozigh01/udemy_KubernetesForAbsoluteBeginners)
* Kubernetes: [site](https://kubernetes.io/)
    * [Documentation](https://kubernetes.io/docs/home/)
    * [Concepts](https://kubernetes.io/docs/concepts/)
        * [Pods](nginx-7db9fccd9b-8m2wp)
    * [Setup](https://kubernetes.io/docs/setup/)
    * [Minikube](https://kubernetes.io/docs/setup/learning-environment/minikube/)
    * [kubeadm](https://kubernetes.io/docs/reference/setup-tools/kubeadm/kubeadm/)
    * [kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
* Local Environment: [Docker for Windows](https://docs.docker.com/docker-for-windows/?utm_source=docker4win_2.1.0.5&utm_medium=docs&utm_campaign=referral)
* Kubernetes Environment: [play with k8s](https://labs.play-with-k8s.com/)
* Google Cloud Platform (GCP):
    * [GCP Free Tier](https://cloud.google.com/kubernetes-engine/)
    * [Kubernetes Engine Docs](https://cloud.google.com/kubernetes-engine/docs/)
    * [Kubernetes Engine](https://cloud.google.com/kubernetes-engine/)
* Play with k8s:
    * [play-with-k8s.com](https://labs.play-with-k8s.com/)

## Notes

### Commands

| Action | Command | Example |
| ---- | ------ | ------- |
| Get list of objects | kubectl get \<objectname\>s | kubectl get pods |
| Get list of all objects | kubectl get all | |
| Create Object from file | kubectl create -f \<filename\> | kubectl create -f replicaset-definition.yml |
| Delete Object | kubectl delete \<object name\> | kubectl delete ReplicaSet myapp-replicaset |
| Delete all Object types | kubectl delete \<objectname\>s --all | kubectl delete pods --all |
| Replace Object | kubectl replace -f \<filename\> | kubectl replace -f replicaset-definition.yml |
| Scale replicaset | using filename | kubectl scale --replicas=6 -f replicaset-definition.yml |
| Scale replicaset | using object type / name| kubectl scale --replicas=4 replicaset myapp-replicaset |


