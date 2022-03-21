# kaniko-poc
### Create secret to hold dockerhub credentials
```kubectl create secret docker-registry regcred --docker-username=<username> --docker-password=<password> --docker-email=<email_id>```

Checking if it was properly created -

```kubectl get secret secret-tiger-docker -o jsonpath='{.data.*}' | base64 -d```

### Creating image of hello_world.py script

```kubectl apply -f create-executor-pod.yaml```

### Running the created image in a pod 

```kubectl apply -f hello-world-pod.yaml```
