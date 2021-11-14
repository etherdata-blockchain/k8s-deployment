# Set up

## Mongodb K8s Operator

1. Create a namespace
`
kubectl create namespace mongodb
`
2. Install dependencies
`
kubectl apply -f https://raw.githubusercontent.com/mongodb/mongodb-enterprise-kubernetes/master/crds.yaml
`
3. Install operator
`kubectl apply -f https://raw.githubusercontent.com/mongodb/mongodb-enterprise-kubernetes/master/mongodb-enterprise.yaml
   `

4. Install ops manager resource
`kubectl apply -f ops-manager.yml`

## Issues

- Do not use hostpath or microk8s default storage for your mongodb cluster, otherwise, you may encounter no such file error
- 

## Resouces

- https://github.com/mongodb/mongodb-enterprise-kubernetes
- 