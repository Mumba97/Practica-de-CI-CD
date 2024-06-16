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










5-se realizan prueas desde git para realizar un push
