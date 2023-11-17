# k8s-api-rust-minikube
api desplegada en kurbenetes mediante minikube
- Despliega 3 pods de tu aplicacion
- Se debe de mantener la integridad de los datos
- El acceso a la APi debe de ser por el dominio api.[primera letra del nobre][apellido].com
- Sube tu liga de flipgrid con la demo de tu programa
    Demo:
          Mostrar los pods, despliegues y servicios ejecutados en k8s.
          Mostrar el accceso via IP (externa del servicio) al API REST
          Muestra un ejemplo agregando un elemento 
          Muestra el listado de todos los elementos
          Mostrar la configuracion del ingress en K8s (Utilizar puerto 80)
          Mostrar el acceso via dominio a la API REST
          Muestra un ejemplo actualizando un elemento
          Muestra el listado de todos los elementos
- Proceso:
- 1: si ya tienes minikube instalado solamente usar el comando -minikube start para que inicie (teniendo en cuenta que vas a usar docker y no otras como virtualbox etc).
- 2: cuando este corriendo usa el comando minikube addons enable ingress para habilitar el controlador de ingress.
- 3: cuando este activado dependiendo de tu sistema debes de modificar el archivo hosts con modo administrador para que se guarde bien y poner el ip de minikube seguido de un espacio y tu nombre de hosts. ejemplo:(127.0.0.1 api.rpenaserrano.com)
- 4: dependiendo de tu sitema operativo tienes que usar el comando minikube tunnel para que funcione bien la direccion ip del ingress.
- 5: ya solamente usar el comando kubectl apply -f nombre_del_archivo.yaml para aplicar los archivos yaml.
- 6: para verificar si estan corriendo bien todo solamente usa el comando kubectl get all para ver que todo este bien.
- 7: ya para finalizar solamente copia tu ip o nombre del hosts seguido del path que definistes en el ingress ejemplo:(api.rpenaserrano.com/pizzas) para poder entrar y vizulizar tu api en el navegador y en caso de 
     querer agregar,actualizar,etc solamente usa postman.
