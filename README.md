# ZypeTest
Pre-requisitos
1.	Instalar Node.JS (https://nodejs.org/en/download/package-manager/)
2.	En línea de comando:
Instalar Newman > npm install -g newman
Instalar el generador de reportes en HTML > npm install -g newman-reporter-htmlextra

Datos de entrada 
1. Zype Env.postman_environment.json - Archivo de ambiente de Potman (con URL y apiKey habilitada)
2. Zype_GetListVideos.postman_collection.json y Zype_GetListPlaylists.postman_collection.json - Requests de las APIs a evaluar
3. GetListVideos.csv y GetListPlaylists.csv - Archivos con 1 o n set de datos para la prueba de la API
PD: Los puntos 1 y 2 se generan desde Postman

Ejecución
1. Para generar reportes GetListVideo, ejecutar por línea de comando
newman run "Zype_GetListVideos.postman_collection.json" -e "C:\Users\rpinango\Downloads\config\Zype Env.postman_environment.json" -d "C:\Users\jvilela\Downloads\data\GetListVideos.csv" -r htmlextra --reporter-htmlextra-title "Zype - GetListVideos"
2. Para generar reportes GetListPlayists, ejecutar por línea de comando
newman run "Zype_GetListPlaylists.postman_collection.json" -e "C:\Users\rpinango\Downloads\config\Zype Env.postman_environment.json" -d "C:\Users\jvilela\Downloads\data\GetListPlaylists.csv" -r htmlextra --reporter-htmlextra-title "Zype - GetListPlaylists"
