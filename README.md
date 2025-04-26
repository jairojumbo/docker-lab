# docker-lab

Repositorio de laboratorio para pruebas y experimentación con **Docker**.

## Autor
- **Usuario GitHub**: [@jairojumbo](https://github.com/jairojumbo)

## Requisitos

Antes de comenzar asegúrate de tener instalado:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/) (opcional, si el proyecto lo requiere)

## Clonar el repositorio

```bash
git clone https://github.com/jairojumbo/docker-lab.git
cd docker-lab
```

## Pasos para ejecutar

1. **Construir la imagen Docker**

```bash
docker build -t docker-lab .
```

2. **Correr el contenedor**

```bash
docker run -d -p 8080:80 --name docker-lab-container docker-lab
```

- `-d`: Ejecuta el contenedor en segundo plano.
- `-p 8080:80`: Mapea el puerto 80 del contenedor al puerto 8080 de tu máquina local.
- `--name docker-lab-container`: Asigna un nombre al contenedor.

3. **Verificar que esté corriendo**

```bash
docker ps
```

Deberías ver `docker-lab-container` en la lista de contenedores activos.

4. **Acceder a la aplicación**

Abre tu navegador y entra a:

```
http://localhost:8080
```

## Comandos útiles

- **Detener el contenedor:**

```bash
docker stop docker-lab-container
```

- **Eliminar el contenedor:**

```bash
docker rm docker-lab-container
```

- **Eliminar la imagen:**

```bash
docker rmi docker-lab
```

## Estructura del proyecto

```plaintext
docker-lab/
├── Dockerfile
├── README.md
└── (otros archivos según sea necesario)
```