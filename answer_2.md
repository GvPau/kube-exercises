# Ejercicio 2

ReplicaSet con las especificaciones: 

![title](images/hw2/replicaset.png)

Creamos el replicaSet con el comando:
**kubectl apply -f replicaset.yaml**

![title](images/hw2/applyreplica.png)

Si hacemos **kubectl get rs** podemos ver el listado de replicasets que tenemos.

![title](images/hw2/getrs.png)

Para que el replicaSet tenga 3 replicas, simplemente se ha especidicado en el yaml

![title](images/hw2/replicas.png)

Si ahora miro los pods, podemos ver que se han creado 2 nuevos pods con la misma configuracion que el pod del ejercicio anterior, por lo tanto podemos ver que tenemos los 3 pods levantados y running.

![title](images/hw2/getpods.png)

Para poder escalar el numero de replicas se tiene que utilizar el comando:
**kubectl scale --replicas=10 -f replicaset.yaml**

Como podemos ver, despres de hacer el scale muestro los pods, verificando que tenemos 10.

![title](images/hw2/scale.png)

Si se necesita tener una replica en cada uno de los nodos de Kubernetes podemos utilizar el object DeamonSet:

Un DaemonSet garantiza que todos (o algunos) de los nodos ejecuten una copia de un Pod. 
Conforme se añade más nodos al clúster, nuevos Pods son añadidos a los mismos. Conforme se elimina nodos del clúster, dichos Pods se destruyen y al eliminar un DaemonSet se limpian todos los Pods que han sido creados.
