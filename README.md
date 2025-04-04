### Escuela Colombiana de Ingeniería

### ARCN - Arquitectura centrada en el negocio.

#  Taller Microservice Basics

Este laboratorio muestra el desarrollo  de los pasos necesarios para crear un microservicio básico "Hello World" utilizando Spring Boot, GitHub, GitHub Codespaces y Play with Docker.

## Desarrollo del laboratorio.

Se configuró el codespace como se indica en el laboratorio de manera que resultó en la siguiente estructura del proyecto:

Resultando en la siguiente estructura del proyecto:

    📂 src
    ├── 📂 main
    │   ├── 📂 java
    │   │   ├── 📂 com
    │   │   │   ├── 📂 arcn
    │   │   │   │   ├── 📂 microservice_helloworld
    │   │   │   │   │   ├── 📄 HelloWorldController.java
    │   │   │   │   │   ├── 📄 MicroserviceHelloworldApplication.java
    📄 Dockerfile

Siendo la estructura del Dockerfile la siguiente: 

```dockerfile
  FROM openjdk:17-jdk-slim 
  COPY target/microservice-helloworld-0.0.1-SNAPSHOT.jar microservice-helloworld.jar 
  ENTRYPOINT ["java", "-jar", "/microservice-helloworld.jar"]
```

### Proceso de creación de contenedor:

Se utiliza el comando:
```bash
  docker build -t microservice-helloworld .
```
![image](https://github.com/user-attachments/assets/b8c51769-652e-4492-80fb-a33895b887f2)

Se crea el tag y adicionalmente se realiza el proceso de logueo y de subir la imagen al repositorio de Docker hub:

```bash
  docker tag microservice-helloworld unandresmasxd/microservice-helloworld 
```

![image](https://github.com/user-attachments/assets/1eec18c0-76ef-40a9-a1b4-a5bde27d9b6f)
![image](https://github.com/user-attachments/assets/20e6dcb5-31f5-4231-8355-c76b3be5d5cf)

### Uso de Play with Docker

Se procedió a acceder a la página web de Play with Docker para poder correr un contendor con la imagen subida en el repositorio de Docker hub:
![image](https://github.com/user-attachments/assets/71d98f6c-2ae2-41af-a653-d31d2d2f2981)
![image](https://github.com/user-attachments/assets/30eccbaf-eabe-4ed0-999f-02d5731ca066)




