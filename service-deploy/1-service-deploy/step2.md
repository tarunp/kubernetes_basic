Now our cluster is up and running, lets install the service in our cluster. Before executing the below script, make sure you have gone through the script and understand all the Yaml properties define in it. Explore the specification in the `my-worksop\book-club.yaml` file that we will use to deploy a stateless service to our cluster.

Let's now deploy this service to our cluster with the following command.

`kubectl apply -f my-workshop/book-club.yaml`{{execute}}

Once deployed, you can check the containers created in the pods of this service with the following command.

`kubectl get pods --selector app=bookclub -n kubernetes-basic  -o jsonpath={.items[*].spec.containers[*].name}`{{execute}}

The previous command might not display results immediately if the pods are not yet created. If you don't receive any results, wait for some time and try executing the previous command again.

A _NodePort_ service can be accessed through any machine on the cluster through the specified `nodePort`. Let's explore our service by navigating to the following URL.

https://[[HOST_SUBDOMAIN]]-30001-[[KATACODA_HOST]].environments.katacoda.com/

> Note: Currently, only the home page of the application is operational because we haven't yet deployed all the supporting microservices that this application requires. You can take that as a exercise to deploy all the services by yourself using Nodeport or by using a service mesh.

i will try to add more examples later.

You can delete the namespace and its services with the following command.

`kubectl delete namespace kubernetes-basic `{{execute}}

Happy Learning!

