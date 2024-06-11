# ExamenArmandM06

# Crear una nova carpeta pel projecte
mkdir projecte-examen
cd projecte-examen

# Inicialitzar un projecte de Node.js
npm init -y

# Instal·lar React
npx create-react-app react-app

# Entrar a la carpeta de l'aplicació React
cd react-app

# Instal·lar json-server
npm install json-server

# Tornar a la carpeta del projecte principal
cd ..

# Crear una carpeta per a Phaser
mkdir phaser-app


El fitxer db.json hauria de crear-se a la carpeta principal del projecte, al mateix nivell que les carpetes react-app i phaser-app. Aquí tens una estructura de carpetes perquè sigui més clar:

css
Copia el codi
projecte-examen/
├── db.json
├── react-app/
│   └── (Fitxers del projecte React)
└── phaser-app/
    └── (Fitxers del projecte Phaser)
Passos detallats per crear el fitxer db.json:
Crear la carpeta del projecte i inicialitzar el projecte de Node.js:

bash
Copia el codi
mkdir projecte-examen
cd projecte-examen
npm init -y
Crear el fitxer db.json al directori principal:

Al directori projecte-examen, crea un fitxer anomenat db.json amb el següent contingut:

json
Copia el codi
{
  "users": [
    { "id": 1, "name": "John Doe" },
    { "id": 2, "name": "Jane Doe" }
  ]
}
Instal·lar json-server:

bash
Copia el codi
npm install json-server
Afegir l'script per iniciar json-server a package.json:

Edita el fitxer package.json i afegeix l'script a la secció de "scripts":

json
Copia el codi
"scripts": {
  "start-json-server": "json-server --watch db.json --port 5000"
}
Executar json-server:

bash
Copia el codi
npm run start-json-server
Amb aquests passos, el fitxer db.json estarà correctament creat i configurat a la carpeta principal del projecte, i json-server podrà utilitzar-lo per proporcionar una API REST falsa per als teus projectes.


Si no tens permisos d'administrador o prefereixes no utilitzar sudo, pots instal·lar http-server localment com a dependència del projecte:

bash
Copia el codi
npm install http-server --save-dev
Després, pots executar http-server des de la carpeta del projecte amb npx:

bash
Copia el codi
npx http-server . -o