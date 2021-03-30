Let's prepare our environment for working through this scenario. In this scenario, we will download and execute a script that will start the Katacoda Kubernetes cluster. In the next step, we will see how to install a Kubernetes deployment and access it via Nodeport service. Execute the following command to download the exercise files that we will use in this scenario.

`git clone https://github.com/tarunp/kubernetes_basic.git; mv kubernetes_basic/scripts/scenario my-workshop; rm -rf kubernetes_basic`{{execute}}

Let's start our cluster with the following command.

`. my-workshop/prepare-cluster.sh`{{execute}}

Let's check the status of our Kubernetes cluster.

`kubectl cluster-info`{{execute}}

Once all the resources are running, press "CTRL+C" to exit the watch. Let's move on to the next step.
