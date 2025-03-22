# Fake Shop


## Variável de Ambiente
DB_HOST	=> Host do banco de dados PostgreSQL.

DB_USER => Nome do usuário do banco de dados PostgreSQL.

DB_PASSWORD	=> Senha do usuário do banco de dados PostgreSQL.

DB_NAME	=>	Nome do banco de dados PostgreSQL.

DB_PORT	=>	Porta de conexão com o banco de dados PostgreSQL.


## principais comandos de linha
 docker build -t gilbertofl/fake-shop:v1
 kubectl apply -f k8s/deployment.yaml 
 kubectl get all
 
 PUBLICANDO:
 docker container ls 
 docker push gilbertofl/fake-shop:v1

 kubectl rollout history deployment fakeshop 
 kubectl rollout undo deployment fakeshop  && watch ‘kubectl get po’ 


## DELETANDO POD E RECRIANDO
kubectl get pod 
NAME                        READY   STATUS    RESTARTS   AGE
fakeshop-bf5c75c95-p4p4n    1/1     Running   0          11m
postgres-84bcf649cd-5mhxc   1/1     Running   0          11m

kubectl delete pod/fakeshop-bf5c75c95-p4p4n

## PARA VER A DISTRIBUIÇÃO NOS PODS
kubectl get pod -o wide
