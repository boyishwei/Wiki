### Common commands

* Install
* Start/stop
  ```
  minikube start --image-mirror-country='cn'
  # login to cluster
  minikube ssh
  # check pod ip
  minikube ip
  # stop minikube
  minikube stop
  # delete cluster
  minikube delete
  ```
* cluster
  ```
  kubectl cluster-info
  ```
* Node
  ```
  kubectl get node -A
  ```
* kubectl
  ```
  kubectl version --client
  ```
