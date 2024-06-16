iii# Practica-de-CI-CD
repositorio publico para prueba 
Pasos para resolver la practica
1. Definir los Requisitos y Objetivos del Pipeline
 crear un pipeline de integración continua que construya, ejecute las pruebas y guarde el artefacto generado (JAR) de la aplicación. 
   
3. Seleccionar Herramientas
4. Configurar el Repositorio de Código
5. Escribir un Archivo de Configuración del Pipeline




1- Priemero se crea el nuevo repositorio en modo publico para esta aplicación, dando clic en your repositories
![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/b624e1cf-8837-44ee-b86f-17873676e5e5)

2- como segundo paso, se le da clic en NEW, para crear un nuevo repositorio 
![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/0faad8e5-9000-4661-848c-afa3cf63612b)

3- se elige el nombre y se configura de manera publica en este caso
![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/f548c834-7f81-430a-b5ee-0149e237ae7c)

4- Se clona el repositorio en el entorno local con git, para poder realizar los push and commit, para esto se da clic en la pestaña code y se copia el link https para realizar la clonacion.
![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/55160ba0-7b5d-4e04-b76d-346b4b173a05)

5- una vez copiado el link se procede a descargar git si es que no se tiene aun instalado en la pc local, se deja link para su descarga 
https://github.com/git-for-windows/git/releases/download/v2.45.2.windows.1/Git-2.45.2-64-bit.exe
una vez descargado e instalado se procede a clonar el repositorio con el comando git clone 
pero antes te debes de posicionar en la carpeta donde quieres realizar el clonado
una vez aqui, con el comando git clone y el link del repositorio previamete copiado se procede a realizar el clonado 
![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/c9c61ec8-a177-4aaf-922e-eab904aa7df1)

6- una vez clonado se pueden realizar cambios de manera local y subirlos al repo remoto

7- se procede a subir el archivo con el codigo, esto puede hacerse desde la maquina local y git o directamente en la consola de github, se muestran ambas maneras 

 a) manera 1
 de manera local 
   se copia la carpeta .zip en la carpeta creada despues de la clonacion en la maquina local
   ![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/8975353f-ca2c-4dcf-9ef3-8455f0e39b2f)

 una vez copiada la carpeta nos ayudamos de git, para ver los status de cambios con el comando git status
 ![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/7c3b358a-6d76-4a0e-be4a-62d4affc77d9)

 vemos que hay cambios que aun no son agregados, por lo que con el comando git add . se agregan 

 ![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/3676865a-5822-4ea9-9987-e184c40d7956)

con esto ya podemos hacer un git commit -m "prueba1" para realizar cambios y comentarlo con alguna etiqueta
![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/6684a2ff-9c15-4c96-8b03-fbd3424803c5)

para finalmente realizar la subida de los cambios realizados se ocupa el comando git push que subira los cambios realizados al repo remoto 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/7fc7b122-f0ef-418f-9e07-701f1b9579b4)

b) desde la consola de github 

se da clic en la pestaña add file u upload files para subir archivos al repo 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/9bc412fd-b5dc-4630-91a9-2308bf22842f)


8- ya con el codigo en el repositorio remoto podemos proceder a realizar la action que se necesita para el pipeline.

Los requerimietos del equipo son que se buscan desplegar el API se debe crear un pipeline de integración continua que construya, ejecute las
pruebas y guarde el artefacto generado (JAR) de la aplicación. 

Para eso se debe configurar el archivo formato .yml , por lo que se da clic en actions 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/85ccdcd2-a05f-4261-957b-16717fd37498)

aqui se le da clic en New workflow 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/11dfeb62-5166-4f9e-842a-2f4d7d3ab2f1)

se pueden seleccionar las herramietas que sean de utilidad para le proyecto, en este caso nos podemos apoyar del template Publish java Package with Maven o java whit maven, ya que el script se incia con Maven 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/dc99aaeb-3c9c-4139-bbcd-2fa0b5c60eaa)

esto nos da un codigo en formato .yml que debemos configurar a nuestra conveniencia para entregar el resultado esperado 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/22474140-50a2-4805-a25a-4de884e244a8)

Para este caso se realizo el siguiente codigo, ya que se busca que despues de cada pull request en la rama main se construya la aplicacion y se publique en formato .jar

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/28fe1ec2-ad6d-4696-8440-b1130d8b6b34)

Para realizar un pull request se debe de crear una nueva rama para comparar con la main, desde git o desde la consola directa de github

- para hacerla desde la consola de git se usa el comando git checkout -b 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/42bbafa2-325c-4b34-9578-067ef1c34bd0)

se crea un archivo con modificaciones y se realiza un git add, un git commit u al final un push

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/0447cb24-ac59-4535-a4d4-f514312ce780)

una vez realizada la carga se regresa a la consola de github y se accede a pull request y se da clic en new pull request 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/f91c202e-616a-4239-b212-5b8e68ec4313)

se eligen las ramas a comparar

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/fb78b125-9406-4e84-bda5-60d689abfe5d)

y se corre el nuevo pull, dando resultados satisfactorios

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/29866192-4106-42f8-b4c8-0eb5dc6914c6)

obteniedo los logs esperados de la creacion 

![image](https://github.com/Mumba97/Practica-de-CI-CD/assets/121688225/2c492509-fbf7-4186-98a9-ef8cf3c5d001)














5-se realizan prueas desde git para realizar un push
