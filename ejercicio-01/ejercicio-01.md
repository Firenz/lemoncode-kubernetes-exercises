# Ejercicio 01
## Pasos parte 1
Si usamos `minikube` para realizarlo, hay que añadir estos pasos extra antes:
```bash
minikube start
minikube docker-env
# To point your shell to minikube’s docker-daemon, run
eval $(minikube -p minikube docker-env)
```

Comandos para realizar la parte 1
```bash
cd todo-app/
docker build . -t lemoncode-kubernetes-ejercicio-01
cd ..
kubectl apply -f todo-app-deployment.yaml
kubectl get deployments
kubectl get pods
```

## Pasos parte 2
Si usamos `minikube` para realizarlo, hay que ejecutar este comando en otra terminal paralela a la de los comandos de la parte 2
```bash
minikube tunnel
```

Comandos para realizar la parte 2
```bash
kubectl apply -f todo-app-loadbalancer.yaml
kubectl get svc
kubectl describe services lemoncode-ejercicio-01-loadbalancer
```

Con la IP obtenida con el comando `kubectl get svc`, abrimos el navegador y nos dirigimos a la ruta `http://REEMPLAZAR_CON_IP_EXTERNA:8080` para ver a la app funcionando.

## Borrar pasos
Comandos para borrar los procesos creados con el ejercicio
```bash
kubectl delete -f todo-app-loadbalancer.yaml
kubectl delete -f todo-app-deployment.yaml
```

Y si hemos `minikube` para realizar el ejercicio: 
1. Cerramos la terminal paralela que ejecuta el comando `minikube tunnel`
2. Ejecutamos `docker rm -f $(docker ps -qa)`
3. Ejecutamos `minikube stop`
4. Cerramos terminal para que se cierren los contenedores de minikube