# PRUEBA 3

CI/CD Dockerizar un nginx con el index.html default. Elaborar un pipeline que ante cada cambio realizado sobre el index.html buildee la nueva imagen y la actualize en la plataforma elegida. (docker-compose, swarm, kuberenetes, etc.) Para la creacion del CI/CD se puede utilizar cualquier plataforma (CircleCI, Gitlab, Github, Bitbucket.)

##

## Prueba de ci/cd
Para la prueba 3 se construye la imagen nginx con alpine ,se crea el dockerfile y se prueba local una vez que funciona se sube el repo y se empieza a crear los action. Primero paso se vincula github con dockerhub para buildear la imagen, se genera token para vincular con github accion y con el token dado se crea una secret "DOCKERHUB_TOKEN" y "DOCKERHUB_USERNAME". Una vez creado se va a action y se crea desde uno del template "Docker image" se especifica el path del index donde va a hacer el check de cada cambio, se colocan los secret y se coloca el tag como latest y que se vaya enumerando a medida que se hagan los action

dockerhub : https://hub.docker.com/repository/docker/mksguti/prueba3/tags?page=1&ordering=last_updated

Para usar aws se crean dos secret actions AWS_ACCESS_KEY_ID y AWS_SECRET_ACCESS_KEY para poder vincular la accion con AWS. Comenzamos en Container Registre donde se crea el repo de la imagen a buildear. Luego se crea la task definition cuando se finaliza se copia el task-definiition.json para pegar en nuestro repositorio. Nos dirijimos a amazon EXS para crear el cluster donde correra las instancias y configuramos el servicio que colocaremos nuestor task,EC2 y cluster creado y le damos un nombre al servicio.
Ahora vamos a nuestro git acction y creamos apartir del template Deploy to Amazon ECS y especificamos los secret,task,path,cluster, container name y servicio. Una vez finalizamos probamos la accion y se puede ver el resultado en :

AWS: http://3.238.195.135/
