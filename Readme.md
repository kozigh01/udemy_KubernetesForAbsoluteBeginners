# Udemy: Kubernetes for the Absolute Beginner

## Resources

* Course: [udemy](https://www.udemy.com/course/learn-kubernetes/)
* Code: [github](https://github.com/kozigh01/udemy_KubernetesForAbsoluteBeginners)
* Kubernetes: [site](https://kubernetes.io/)
    * [Documentation](https://kubernetes.io/docs/home/)
    * [Concepts](https://kubernetes.io/docs/concepts/)
        * [Pods](nginx-7db9fccd9b-8m2wp): [pod template](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/#pod-templates)
        * [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/): [template](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/#example)
        * [Service](https://kubernetes.io/docs/concepts/services-networking/service/): [template](https://kubernetes.io/docs/concepts/services-networking/service/#defining-a-service)
        * [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/): [template](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#creating-a-deployment)
        * [Namespaces](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)
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
* Yaml: [linter](http://www.yamllint.com/)
* Docker/Kubernetes Sample Apps:
    * [Example Voting App](https://github.com/dockersamples/example-voting-app)

### Commands

| Action | Command | Example |
| ---- | ------ | ------- |
| Get list of objects | kubectl get \<objectname\>s | kubectl get pods |
| Get list of all objects |  | kubectl get all |
| Get info about object | kubectl describe \<objectname\> | kubectl describe replicaset.apps/myapp-replicaset |
| Get info about objects | kubectl describe \<kind\> | kubectl describe pod |
| Create Object from file | kubectl create -f \<filename\> | kubectl create -f replicaset-definition.yml |
| Delete Object | kubectl delete \<object name\> | kubectl delete ReplicaSet myapp-replicaset |
| Delete all Object types | kubectl delete \<objectname\>s --all | kubectl delete pods --all |
| Replace Object | kubectl replace -f \<filename\> | kubectl replace -f replicaset-definition.yml |
| Scale replicaset | using filename | kubectl scale --replicas=6 -f replicaset-definition.yml |
| Scale replicaset | using object type / name| kubectl scale --replicas=4 replicaset myapp-replicaset |
| Create deployment |  | kubectl create -f deployment-definition --record |
| Create deploymnet from image | kubectl run \<deployment-name\> --image=\<image-name\> | kubectl run nginx --image=nginx |
| rollout status | kubectl rollout status \<deployment-name\> | kubectl rollout status deployment/myapp-deployment |
| rollout history | kubectl rollout history \<deployment-name\> | kubectl rollout history deployment/myapp-deployment |
| rollout history | kubectl rollout history deployment \<deployment-name\> | kubectl rollout history deployment myapp-deployment |
| apply changes | kubectl apply -f \<\> --record | kubectl apply -f deployment-definition.yml --record |
| apply all changes in directory | kubectl apply -f \<path-to-dir\> | kubectl apply -f . |
| change image | kubectl set image \<deployment-name\> \<image-name\>=\<tagged-image-name\> --record | kubectl set image deployment/myapp-deployment nginx=nginx:1.9.1 --record |
| Rollback deployment | kubectl rollout undo \<deployment-name\> | kubectl rollout undo deployment/myapp-deployment |
| Get node info |  | kubectl get nodes -o wide |
| SSH to Pod |  | kubectl exec -it myapp-deployment-6cc5db4774-424jq bash |
| Test service | node ip from "Get node info"/port from service | curl http://localhost:30008 |
