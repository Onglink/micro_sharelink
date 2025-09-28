PROJETO DE MICRO SERVIÇO PARA COMPARILHAMENTO DE LINK DA PUBLICAÇÃO DO FEED

Tecnologia usada: NODE.JS

instalação de dependencias:
npm init -y
npm install express mongoose nanoid dotenv


banco de dados: MongoDB


Estrutura de pastas:<br>
micro-share-link/<br>
├── models/<br>
│   └── SharedLink.js         # Modelo do MongoDB<br>
├── routes/<br>
│   └── shareLink.js          # Rota principal do serviço<br>
├── controllers/<br>
│   └── shareLinkController.js # Lógica de geração e salvamento<br>
├── .env                      # Configurações sensíveis<br>
├── server.js                 # Ponto de entrada do micro serviço<br>
├── package.json              # Dependências e scripts<br>
