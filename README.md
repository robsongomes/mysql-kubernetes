# Deploying

Deploying the project is easy with kustomize. The **kustomization.yml** defines the sequence of applying resources. Use the command below to deploy Mysql.

`$ kubectl apply -k .`

If you prefer, you can apply each file individually:

`$ kubectl apply -f mysql-configmap.yml`

# Accessing

After deploying the project, kubernetes will expose the following service:

- mysql on ports:
  - 30306 (external)
  - 3306  (internal)