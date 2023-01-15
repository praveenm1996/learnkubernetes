# learndocker
uploading my basic project for the reference
#command to copy sql file to the db in the container 
manual cmd /c "docker exec -i 84e26e303757 mysql -uroot -pexample company1  < usersmain.sql"
#added new dockerfile for DB

Compose command 
docker compose up -d
To down
docker compose down 


15 Jan 2022

Added another folder php-app\page2 and files Dockerfile and index.php  and created new image using Docker build  name used in app2 deploy file.

Run kubectl apply for all four deploy file 
check multi front end pod with different NodePort app 30009,30012 first page , second page.

PS E:\Devops\Docker\learnkubernetes\php-kube-app\k8s> kubectl apply -f .\php-db-deployment.yaml
deployment.apps/db created
service/db created
PS E:\Devops\Docker\learnkubernetes\php-kube-app\k8s> kubectl apply -f .\php-app-deployment.yaml
deployment.apps/app-php created
service/app-php-srv created
PS E:\Devops\Docker\learnkubernetes\php-kube-app\k8s> kubectl apply -f .\php-app2-deployment.yaml
deployment.apps/app1-php created
service/app1-php-srv created
PS E:\Devops\Docker\learnkubernetes\php-kube-app\k8s> kubectl apply -f .\php-adminer-deployment.yaml
deployment.apps/app-adminer created
service/app-adminer-srv created

CHECK http://localhost:30009/ ,http://localhost:30012/  Success

