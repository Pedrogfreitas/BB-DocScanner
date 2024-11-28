
# BB TechDoc

Este repositório refere-se a um projeto de residência acadêmica em parceria com o Banco do Brasil. O objetivo do projeto é analisar imagens e arquivos, extraindo as informações necessárias conforme as solicitações dos usuários.

### Protótipo de Alta Fidelidade 

[![Visualizar no Figma](https://img.shields.io/badge/Visualizar%20no%20Figma-303133?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/design/Mon05F0Mhd1232P0KE80bc/TechDoc?node-id=0-1&node-type=canvas)

### Acessar a Aplicação Online
- Abra seu navegador e acesse https://bbtechdoc.onrender.com/ para ver a aplicação em funcionamento.

### Acessar as rotas da aplicação (swagger)
- Abra seu navegador e acesse https://techdoc.onrender.com/docs

## Stack utilizada

**Front-end:** HTML, CSS, JavaScript

**Back-end:** Python

## Instalação

Abra seu terminal e execute o seguinte comando para clonar o repositório:

 ```bash
git clone https://github.com/Pedrogfreitas/BB-DocScanner

Para fazer as aplicações funcionarem, utilizamos o venv.
```bash
  python -m venv .venv
```
Para a nossa Api, utilizamos o flask.
```bash
  pip install flask
```
Para a documentação da Api utilizamos flask restx.
```bash
    pip install flask_restx
```
Para aceitar as requisições, utilizamos o flask cORS.
```bash
    pip install flask_cors
```
Para digitalizar imagens, utilzanos o pytesseract.
```bash
    pip install pytesseract
```
Para digitalizar pdf, utilzamos o PyPDF2.
```bash
    pip install PyPDF2
```
Para processamento de linguagem natural, utilizamos o spacy.
```bash
    pip install spacy
```
Para rodar a api.
```bash
    python main.py
```

## Comandos de busca:

```bash
quem pagou
quem recebeu
todos os nomes
cpf
cnpj
número da nota
número nf
telefone
endereço
e-mail
número do protocolo
nome do consumidor
descrição do problema
relato do consumidor
pedido
data de emissão
valor
forma de pagamento
destinatário
chave de acesso
informações complementares
produtos
icms
pis
cofins
```

## Documentação da API

#### Para rodar o swagger do projeto:

```http
  /docs
```

#### Endpoint de scanner, para analisar o arquivo

```http
  POST /scan
```

| key   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `file` | `file` | **Obrigatório**. Arquivo que vai ser analisado
| `message` | `string` | **Obrigatório**. O que vai ser procurado dentro do arquivo |

