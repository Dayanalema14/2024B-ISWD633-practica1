# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

![image](https://github.com/user-attachments/assets/34fb411b-7396-489f-8a3f-6aabca3aff4d)


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

![image](https://github.com/user-attachments/assets/a1eb6651-16bf-4535-93f0-d14043654762)


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 

![image](https://github.com/user-attachments/assets/745e36d6-863c-4c7a-82ff-37059bf0562a)


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](img/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

![image](https://github.com/user-attachments/assets/3bcffb03-0ebb-4b68-bd05-397c078298ed)


**¿Qué sucede luego de la ejecución del comando?**

![image](https://github.com/user-attachments/assets/7c3523bb-83d8-4d77-a48f-a114e1f671ed)

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

![image](https://github.com/user-attachments/assets/c536fa81-6eca-40b8-868b-86a17313d4d1)


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 

![image](https://github.com/user-attachments/assets/d3f144a3-bcc4-463f-974f-d8453d136715)


Verificar que el contenedor que se eliminó

![image](https://github.com/user-attachments/assets/9f8684a4-441b-47ff-8377-66fccefa50ed)

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

![image](https://github.com/user-attachments/assets/a1fb215f-3829-4a1d-af60-d11567c07564)


Verificar que el contenedor que se eliminó

![image](https://github.com/user-attachments/assets/d7938c1d-53e5-47f9-94b3-19a5091c8a94)

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
![image](https://github.com/user-attachments/assets/d71f684b-3755-40c5-a200-a988de33b284)

