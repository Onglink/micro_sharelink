PROJETO DE MICRO SERVIÇO PARA COMPARTILHAMENTO DE LINK DA PUBLICAÇÃO DO FEED

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

Para realização de testes:<br>
No terminal, dentro da paras do micro serviço executar:<br>
node server.js<br>
O retorno deve ser:<br>
Micro serviço rodando na porta 3000<br>
<br>
Usando Postman:<br>
Colocar na URL da requisição:<br>
http://localhost:3000/share-link<br>
<br>
Usar o método POST<br>
<br>
Entra no ambiente BODY e inserir os dados abaixo, usando formato JSON (selecionar a opção raw)<br>
{<br>
  "publicationId": "abc123",<br>
  "userId": "usuário456",<br>
  "channel": "exemplo"<br>
}<br>
<br>
Deverá receber o retorno dessa forma:<br>
{<br>
    "shortUrl": "https://sua.plataforma.com/p/abc123?ref=exemplo&uid=usuário456&s=4p85nfL0"<br>
}<br>


