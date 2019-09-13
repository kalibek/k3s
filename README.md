k3s server for local experiments
================================

docker compose file is taken from [k3s](https://k3s.io) which is a nice tool to start with kube

What is it?
----------

it is `docker-compose.yaml` with additional nginx container to run local kubernetes and be able to expose applications on localhost

How to use?
-----------

1. cd into project directory and just `docker-compose up -d --scale node=3` and then apply your deployment and you can access it at http://localhost:9000. 
2. copy `kubeconfig.yaml` to be able to connect to your cluster. `cp kubeconfig.yaml ~/.kube/config`
3. There is hello-world deployment template in this application borrowed from https://github.com/paulbouwer/hello-kubernetes. just run `kubectl apply -f hello-kubernetes.yaml`

