
  # Interfaz e-commerce universitaria

  Diseño realizado por medio de Figma: https://www.figma.com/design/mCxnv7Io5CwXjQ5gg5WgCl/Interfaz-e-commerce-universitaria.

  ## Ejecutando el codigo

  Ejecuta `npm i` para instalar las dependencias.

  ## Dependencias y versiones
  - Node.js: `v22.19.0`
  - npm: `11.14.0`

  Consulta las dependencias y sus versiones en `package.json` (y las versiones fijadas en `package-lock.json`). Para ver las versiones de las herramientas y las dependencias instaladas, ejecuta:

  - Dependencias directas: `npm list --depth=0`
  - React y React DOM, si están instalados: `npm list react react-dom`

  Ejecuta `npm run dev` para inicar el servidor como desarrollo.

  ## Desplegar en firebase hosting

  # Los puntos 1,2 y 3 se hace unicamente cuando se inicia el proyecto en otro equipo nuevamente

  1. Instala Firebase CLI: `npm install -g firebase-tools`.
  2. Inicia sesión: `firebase login`.
  3. Configura Firebase Hosting: `firebase init hosting`.
  4. Genera la aplicación: `npm run build`.
  5. Despliega: `firebase deploy --only hosting`.

  ### Configuración de Firebase y variables de entorno

  Si la aplicación usa Firebase desde el cliente, configura sus credenciales en un archivo `.env` local, siguiendo los nombres de variables que espera el código (por ejemplo, `VITE_FIREBASE_API_KEY`, `VITE_FIREBASE_AUTH_DOMAIN`, `VITE_FIREBASE_PROJECT_ID`, `VITE_FIREBASE_STORAGE_BUCKET`, `VITE_FIREBASE_MESSAGING_SENDER_ID` y `VITE_FIREBASE_APP_ID`). En proyectos con Vite, las variables disponibles en el navegador deben llevar el prefijo `VITE_`.

  No subas `.env` al repositorio: añádelo a `.gitignore` y comparte los nombres requeridos mediante un archivo `.env.example` sin valores reales. Configura también estas variables en el entorno de compilación de tu proveedor antes de ejecutar `npm run build`; Hosting no las obtiene automáticamente de tu archivo local. Si cambian, vuelve a compilar y desplegar.

  La API key de Firebase para aplicaciones web suele ser identificadora del proyecto, no un secreto ni un sustituto de reglas de seguridad. Restringe su uso cuando corresponda y protege los datos con reglas de Firebase. Nunca incluyas credenciales de cuentas de servicio ni claves privadas en variables `VITE_` o en el código del navegador.

    ### Servicios de Firebase utilizados

    - **Authentication (Auth):** gestiona el registro, inicio y cierre de sesión, y permite identificar a los usuarios para controlar el acceso.
    - **Cloud Firestore:** base de datos NoSQL para guardar y consultar los datos de la aplicación, como productos e información relacionada con usuarios.
    - **Cloud Storage:** almacena archivos, por ejemplo, imágenes de productos. Para usar Storage en este proyecto, es necesario actualizar el proyecto de Firebase al plan **Blaze** (pago por uso); el consumo puede generar cargos.
    - **Firebase Hosting:** publica y sirve la aplicación web compilada en Internet. El despliegue se realiza con `firebase deploy --only hosting`.


  
  
 
  