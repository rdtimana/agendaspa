# Guía de Instalación

## Prerrequisitos

1. Asegúrate de tener instalado [Node.js](https://nodejs.org/) (versión X o posterior).
2. Instala [npm](https://www.npmjs.com/) (que generalmente se instala con Node.js).
3. Tener acceso a una base de datos compatible con la aplicación (por ejemplo, MySQL, PostgreSQL).

## Configuración de la Base de Datos

1. Crea una base de datos nueva a través de tu gestor de bases de datos.
2. Configura el archivo de configuración (config/database.js) con los detalles de tu base de datos.
3. Ejecuta las migraciones y semillas para poblar la base de datos inicial. Usa el siguiente comando:
   
   ```
   npm run migrate
   ```

## Ejecutar la Aplicación

1. Clona el repositorio en tu máquina local:
   
   ```
   git clone https://github.com/rdtimana/agendaspa.git
   ```

2. Navega al directorio del proyecto:
   
   ```
   cd agendaspa
   ```

3. Instala las dependencias del proyecto:
   
   ```
   npm install
   ```

4. Ejecuta la aplicación:
   
   ```
   npm start
   ```