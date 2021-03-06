# Autotune en Docker

En este repositorio encontrará archivos que le permiten usar un contenedor con el software [autotune](https://github.com/adamcw/autotune). 

A continuación una descripción de los archivos en este repositorio.

* [Dockerfile](Dockerfile) este archivo le permitirá construir su contenedor de Autotune. Para construir este contenedor usted debe tener [instalado Docker](https://docs.docker.com/engine/installation/) en su computador. 
Una vez lo tenga instalado puede ejecutar el siguiente comando para crear su contenedor con Autotune 
```
docker build -t autotune .
```

* [run.sh](run.sh) Este archivo le permitirá correr el contenedor de la siguiente manera<sup>[1](#dockerinstalado)</sup>.
```
./run.sh josanabr/autotune example_runs.json 
```
donde el archivo .json tiene la configuración de la ejecución que se desea hacer. 
Este archivo debe estar en el directorio donde se ejecuta el script.

En caso de tener problemas con la ejecución del script valide que este tenga permisos de ejecución o ejecute `chmod +x run.sh` para garantizar que el script tenga permisos de ejecución.

* [submit.condor](submit.condor) Este archivo permite la ejecución del contenedor de autotune a través de HTCondor.

* [example_runs.json](example_runs.json) Archivo .json con datos de prueba para ejecutar en el contenedor.

---

<a name="dockerinstalado">[1]</a> se asume que usted ya tiene instalado Docker en su computador.
