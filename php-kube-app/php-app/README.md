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

CHECK http://localhost:30009/ ,http://localhost:30012/  Success

TODO Ingress deploy 
Learn Ingress:
Follow : https://devopscube.com/kubernetes-ingress-tutorial/
need to install all prerequisite for ingress
Follow : https://devopscube.com/setup-ingress-kubernetes-nginx-controller/

------
install all prerequisite buy download the repo and open in new VS code kubectl apply  all the  file in the folder manifests
IN windows rename hostname 

open cmd in admin rights 

C:\Windows\system32>cd drivers

C:\Windows\System32\drivers>cd etc

C:\Windows\System32\drivers\etc>notepad hosts

Add the line in the file
127.0.0.1  praveensite.com

create ingress-srv.yaml file 

convert the Nodeport to ClusterIP in the app and app2 deploy file .

Run the deploy file 

http://praveensite.com/app1   => app
http://praveensite.com/app2   => app2

 Usefull link : https://stackoverflow.com/questions/65703968/kubernetes-ingress-nginx-use-regex-to-match-exact-url-path
                https://stackoverflow.com/questions/52021925/kubernetes-ingress-non-root-path-404-not-found
                https://kubernetes.io/docs/concepts/services-networking/ingress/
                https://kubernetes.github.io/ingress-nginx/examples/rewrite/


