PROJETO DE MICRO SERVIÇO PARA COMPARTILHAMENTO DE LINK DA PUBLICAÇÃO DO FEED

Tecnologia usada: <br>
Node.js<br>
Express<br>
MongoDB<br>
NanoID<br>
Dotenv<br>


<br><br>
Estrutura de pastas:<br>
micro-share-link/<br>
├── models/<br>
│   └── shareLinkModel.js         # Modelo do MongoDB<br>
├── routes/<br>
│   └── sharedLinkRoutes.js          # Rota principal do serviço<br>
├── controllers/<br>
│   └── sharedLinkControllers.js # Lógica de geração e salvamento<br>
├── .env                      # Configurações sensíveis<br>
├── server.js                 # Ponto de entrada do micro serviço<br>
├── package.json              # Dependências e scripts<br>
<br><br>

<b>Instalação do micro serviço:</b>
<b>Clone ou faça o download do repositório</b>
git clone https://github.com/Onglink/micro_sharelink.git
cd micro_sharelink

<b>Abra os arquivos no VSCODE</b>

<b> Instale as dependencias através do terminal:</b>
npm init -y
npm install express mongoose nanoid dotenv

<b>Configure o arquivo .env:</b>
PORT=3000
MONGODB_URI=mongodb://localhost:27017/share-link
BASE_URL=https://sua.plataforma.com

<br><br>

<b>Para realização de testes:</b><br>
No terminal, dentro da pasta raiz do micro serviço (micro_sharelink) executar:<br>
node server.js<br>
<b>O retorno deve ser:</b><br>
Micro serviço rodando na porta 3000<br>
<br>

<b>Usando Postman:</b><br>
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
Retorno esperado:<br>
{<br>
    "shortUrl": "https://sua.plataforma.com/p/abc123?ref=exemplo&uid=usuário456&s=4p85nfL0"<br>
}<br>


