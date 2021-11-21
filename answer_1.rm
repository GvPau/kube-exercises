# Ejercicio 1

Pod con las especificaciones: 

![title](images/hw1/podyaml.png)

Creamos el pod con el comando:
**kubectl aplly -f nginx.yaml**

![title](images/hw1/applypod.png)

Si hacemos **kubectl get pods** podemos ver el listado de pods que tenemos.

![title](images/hw1/getpods.png)

Para obtener las ultimas 10 linias de la salida estandas podemos usar el comando:
**kubectl logs --tail=10 nginxpod**

![title](images/hw1/logs.png)


Para poder obtener la ip interna del pod podemos ejecutar el comando:
**kubectl describe pod nginxpod**

![title](images/hw1/descpot.png)


Para poder entrar dentro del pod, podemos ejecutar el siguiente comando:
**kubectl exec -it nginxpod bash**

![title](images/hw1/execpot.png)

Para poder ver el contenido que expone nginx, primero entramos en el pod a partir del ultimo comando mostrado y una vez dentro podemos lanzar un curl al puerto default de nginx, es decdir a http://localhost:80 y podemos ver que nos responde correctamente

![title](images/hw1/curl.png)


Para poder ver la qos establecida al pod, podemos ejecutar el comando:
**kubectl get pod nginxpod --output=yaml**
Y al final del log podemos ver la qos que kubernetes ha otorgado al pod


![title](images/hw1/qos.png)

La razon por la que se ha assignado al pod el qos "Guarenteed" es porque los limits y los requests son iguales entre ellos (siendo los dos diferentes de 0).


