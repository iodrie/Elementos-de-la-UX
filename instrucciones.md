# Cómo usar este repositorio

En este repositorio iremos recogiendo todos los contenidos que generéis durante las reuniones de expertos, en las que trabajaréis contenidos adicionales sobre la asignatura que no presentaremos durante las clases expositivas.

Para incorporar estas aportaciones, utilizaremos el flujo de trabajo que ya has visto en los tutoriales que has realizado: fork a tu cuenta personal, branch con las modificaciones concretas en las que estés trabajando, y pull request para incorporar tus cambios al repositorio central. 

## La primera vez que lo uses

Vamos a aprovechar la configuración del entorno de trabajo con este repositorio para recordar la manera concreta de aplicar este flujo de trabajo y al mismo tiempo dejar ya preparado el repositorio para cuando empecemos con el trabajo _de verdad_. 

1. Crea un fork de este repositorio en tu cuenta personal. Haz clic en el botón **Fork** que tienes en la parte superior derecha de la pantalla.
2. Clona tu copia personal a tu ordenador. 
    1. En tu navegador, asegúrate de que estás viendo tu fork y haz clic sobre el botón verde **Clone or download**. Copia la URL. 
    2. En la terminal, accede a la carpeta en la que almacenes tus repositorios git, y utiliza el comando `git clone URL-COPIADA-ANTES`. Esto creará la carpeta `Elementos-de-la-UX` en tu ordenador.
3. Crea un branch llamado `añadir-TUNOMBREDEUSUARIO` (por ejemplo, `añadir-mberasategi`) para hacer los cambios correspondientes a la incorporación de tu nombre, y cámbiate a esa rama: `git checkout -b NOMBERDETUBRANCH`
4. Utiliza Sublime Text para crear un archivo llamado `TUNOMBREDEUSUARIO.md`  y guárdalo en una carpeta nueva llamada `estudiantes` dentro del repositorio `Elementos-de-la-UX`.
5. Copia este texto en el archivo recién creado y sustituye con tus datos (nombre y apellido y nombre de usuario y URL del perfil de GitHub):
```
Miren Berasategi :octocat: [@mberasategi](http://github.com/mberasategi)
```
5. Añade si quieres más líneas con más información acerca de ti y guarda el archivo. Asegúrate de hacerlo en el directorio `estudiantes` del repositorio `Elementos-de-la-UX`.
6. Vuelve a la terminal, comprueba que git ha reconocido los cambios con `git status`, y añade todos los cambios para el siguiente commit con `git add .`. Después, haz commit utilizando un mensaje descriptivo, por ejemplo, `git commit -m "Añadir TUNOMBREDEUSUARIO al directorio de estudiantes"`
7. Actualiza tu fork en GitHub con los cambios que acabas de hacer en tu ordenador: `git push origin NOMBREDETUBRANCH`
8. Accede al [repositorio central de Elementos de la UX](https://github.com/DeustoPWEB2018/Elementos-de-la-UX) y crea [un nuevo pull request](https://github.com/DeustoPWEB2018/Elementos-de-la-UX/compare) para incorporar tus cambios. 
    - Si aparece tu recién creado branch, simplemente haz clic en **Compare & pull request**
    - Si no, es posible que tengas que hacer clic en _compare accross forks_. En cualquier caso:
        - **Base fork** debe ser el repositorio central (en DeustoPWEB2018), branch `master`
        - **Head fork** debe ser tu fork personal, branch `añadir-TUNOMBREDEUSUARIO`
        - Haz clic en **Create pull request**
9. ¡Sigue las instrucciones en el propio pull request para terminar!

Con esto ya tendrás una copia personal del repositorio de contenidos adicionales en tu cuenta de GitHub, que utilizarás a lo largo de todo el semestre. La manera de trabajar será prácticamente idéntica para las modificaciones futuras en este repositorio, tal y como se detalla en el siguiente apartado.

## Aportaciones del trabajo con expertos

:construction: Detalles en breve :construction:

### Autoevaluaciones

Solamente la primera vez, es necesario que actualices tu fork con los cambios del repositorio central, que incluyen la plantilla para la autoevaluación. Para esto, accede a la carpeta del repositorio con tu terminal y ejecuta los siguientes comandos:
```
git remote add upstream https://github.com/DeustoPWEB2018/Elementos-de-la-UX.git
git fetch upstream
git checkout evaluaciones
git push origin evaluaciones
```

Después, cada vez que participes en una sesión de trabajo en grupos expertos:

1. En la terminal, accede a tu carpeta del repositorio y cámbiate al branch `evaluaciones`: `git checkout evaluaciones`
2. Abre la carpeta en tu Explorador de archivos (Windows) o Finder (Mac). Verás que ahora, en lugar de mostrar los contenidos trabajados acerca de los elementos de la UX, solamente tienes un directorio `evaluaciones`. Abre el archivo Excel que tienes en esa carpeta (`MiApellidoMiNombre-2018MMDD.xlsx`)
3. Rellena en esa hoja de cálculo tus evaluaciones (para ti y el resto de miembros que han trabajado contigo en el grupo de expertos), siguiendo las indicaciones que encontrarás en el mismo documento. Guárdalo modificando el nombre como corresponde, por ejemplo, `BerasategiMiren-20181002.xlsx` (con `Archivo > Guardar como`)
4. En la terminal, guarda, confirma y envía a tu copia personal en la nube los cambios realizados:
    ```
    git add .
    git commit -m "Evaluar reunión del día 20181002"
    git push origin evaluaciones
    ```
5. Vuelve a tu branch de trabajo para seguir generando el contenido que te corresponde en este borrador: `git checkout TUNOMBRE-TEMA`

Estas autoevaluaciones no necesitan incorporarse al repositorio central, por lo que no es necesario que crees un pull request para esto. Las recogeré del repositorio personal de cada estudiante.
