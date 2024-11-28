<div align="justify">

## Tarea 5

- [Práctica 01](#práctica-01)
    - [Práctica 01.1](#práctica-011)
    - [Práctica 01.2](#práctica-012)
    - [Práctica 01.3](#práctica-013)
    - [Práctica 01.4](#práctica-014)
    - [Práctica 01.5](#práctica-015)
    - [Práctica 01.6](#práctica-016)

***

### Práctica 01

#### Práctica 01.1

> 📂
> Descargar e iniciar un contenedor MariaDB. Ejecuta el siguiente comando para descargar la imagen oficial de MariaDB y crear un contenedor:
>

- Comando:
```bash
docker run --name mariadb-container -e MYSQL_ROOT_PASSWORD=admin -e MYSQL_DATABASE=exampledb -p 3306:3306 -d mariadb:latest
```

- Captura:
<div align="center">
<img src="./img/p1-1.png"/>
<img src="./img/p1-2.png"/>
</div>

<br>

***

#### Práctica 01.2

> 📂
> Verificar logs en caso de problemas
Si la aplicación de ejemplo tampoco funciona, revisa los logs de Tomcat para detectar posibles errores:
>

En este caso no han habido ninguna incidencia. 

```bash
docker logs -f mariadb-container
```

- Captura:
<div align="center">
<img src="./img/p1-3.png"/>
</div>

</br>

***


#### Práctica 01.3

> 📂
> Puedas o no acceder, intenta usar la IP del contenedor Docker (que puedes obtener con docker inspect).
>


```bash
docker inspect mariadb-container
```

- Salida:
```bash
[
    {
        "Id": "04b20019f71a7678924c6f7758f852573d5e488b290cb154dc834bdbb2105c34",
        "Created": "2024-11-27T16:03:30.271178131Z",
        "Path": "docker-entrypoint.sh",
        "Args": [
            "mariadbd"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 49268,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2024-11-27T16:03:31.62774727Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:052f9e69b7b03f7464f4579766e30a795ebf8e93c65cf47698e2869bf882bbe3",
        "ResolvConfPath": "/var/lib/docker/containers/04b20019f71a7678924c6f7758f852573d5e488b290cb154dc834bdbb2105c34/resolv.conf",

        ...
    }
]
```

</br>

***

#### Práctica 01.4

> 📂
> Descargar y ejecutar CloudBeaver en Docker
Ejecuta el siguiente comando para iniciar un contenedor de CloudBeaver:
>

- Comandos:
```bash
docker run -d --name cloudbeaver -p 8978:8978 dbeaver/cloudbeaver:latest

docker ps -a
```


- Captura:
<div align="center">
<img src="./img/p1-4.png"/>
<img src="./img/p1-5.png"/>

</div>

</br>

***


#### Práctica 01.5

> 📂
> Acceder a la interfaz de CloudBeaver
Abre un navegador web.
Navega a la dirección http://localhost:8978.
Sigue las instrucciones de configuración inicial.
Realiza la configuración del cliente.
>

- Captura:
<div align="center">
<img src="./img/p1-6.png"/>
<img src="./img/p1-7.png"/>

</div>

Podemos apreciar como podemos logearnos perfectamente con nuestro administrador. Aquí podemos apreciar el perfil del admin.

- Captura:
<div align="center">
<img src="./img/p1-8.png"/>
</div>
</br>

***

#### Práctica 01.5

> 📂
> Conectar CloudBeaver a MariaDB
>

- Captura:
<div align="center">
<img src="./img/p1-9.png"/>
<img src="./img/p1-10.png"/>
<img src="./img/p1-11.png"/>
<img src="./img/p1-12.png"/>
</div>



<br>
***

#### Práctica 01.7

> 📂
> Conectar CloudBeaver a MariaDB
>

- Captura:
<div align="center">
<img src="./img/p1-9.png"/>
<img src="./img/p1-10.png"/>
<img src="./img/p1-11.png"/>
<img src="./img/p1-12.png"/>
</div>



<br>
***