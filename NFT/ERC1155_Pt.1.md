# Como criar SUA COLEÇÃO DE NFT sem SABER PROGRAMAÇÃO (By MultMcGame#8099)

# PARTE I

- Tokens ERC1155 são utilizados em games na BSC e Polygon(MATIC), que são bem mais baratos, porém possuem valorização menor

## Programas Usados para criação de NFTs!

- Sublime (sublime_text_build_4126_x64_setup)
- Node JS (node-v16.14.0-x64)
- PowerShell do Windows
- Visual Studio Code (VSCodeUserSetup-x64-1.64.2)
- Arquivo Hashlips + Contrato (https://drive.google.com/file/d/1UD1JWqbF68RP8TEjI5XcZRCd1E_QkIlN/view?usp=sharing)
#
- Instalar NODE JS e SUBLIME
- Colocar a pasta hashlips e c:
- Abrir o PowerShell do Windows e Digitar:
- digitar: cd..
- digitar: cd..
- cd hashlips
- node install

OBS:
Caso ocorra o algum tipo: Erro comando "node install", e para resolver isso é bem simples, dentro da pasta "hashlips" é só você apagar a pasta "node_modules" e após isso, execute o PowerShell e ao invés de colocar o comando "node install", coloque o comando "npm install"... esse comando irá fazer a mesma coisa que o "node install"...

- Criar a pasta das camadas dentro da pasta "layers" deixei alguns exemplos na pasta já pronta, mas atenção coloquei muitos exemplos para facilitar e lhe ajudar em ideias, apague as que não vão usar e crie as que achar melhor de acordo com as camadas do seu projeto, Lembrando...coloque em inglês, segue abaixo algumas sugestões:
  - Accessories - Acessórios
  - Background - Fundo
  - Body - Corpo
  - Earring - Brinco
  - Eyes - Olhos
  - Eyewear - Óculos
  - Face - Face
  - Clothing - Roupas
  - Nose - Nariz
  - Fur - Pele
  - Hats - Chapéu
  - Head - Cabeça
  - Mouth - Boca
  - Hair - Cabelo
  - Mouth - Boca
  - Facial Hair - Pêlos faciais
  - Palito de dente - Toothpick
  - Scarf - Cachecol
  - Shirt - Camisa
  - Tail - Rabo
  - Teeth - Dentes
  - Environmment - Meio Ambiente
  - Tongue - Língua 
#
- Abrir o sublime
- Clicar em "File"
- Clicar em "Open"
- Selecionar a pasta hashlips e abrir

Na Pasta SRC vai ter um arquivo chamado config.js

1. Na linha 8 coloque o nome do seu projeto (Preferência em inglês)
2. Na linha 9 coloque a descrição do seu projeto (Preferência em inglês)
3. Na linha 10 coloque o ipfs do seu projeto (O que esta será substituído pelo o da sua coleção, que vou ensinar na próxima aula)
4. Na linha 15 (growEditionSizeTo) será estipulado a quantidade de NFTs gerados nesta coleção, deixei 10 mude como achar melhor. Quanto maior a quantidade, melhor terá que ser o pc e mais demorado fica.
5. Na linha 16 abaixo de (layersOrder) abaixo

Vai ter o nome das mesmas pastas que criei dentro da pasta "layers"
DEIXE IGUAL! como vc criou as suas! apague as linhas ou crie de acordo com a sua coleção, mais não erre na formatação de texto.

OBS: O tamanho das NFTs estão configuradas para o tamanho de 663 x 758 conforme a linha 48 e 49 (substitua de acordo com o tamanho das suas camadas

## Como definir raridade.

As raridades são definidas por # + um número como no exemplo abaixo deixei 9 mas fica ao seu gosto:
Quanto maior o número maior é o peso, resumindo mais comum ela é:

- #1
- #2
- #3
- #4
- #5
- #6
- #7
- #8
- #9

Exemplos fictício de raridade para explicar os números:

- Premium
- Mythical
- Legendary
- Epic
- Super Rare
- Rare
- Uncommon
- Common
- Abundant

Vamos supor que iremos criar o background.
Então dentro desta pasta "background" você vai fazer 9 layer de fundo e renomear elas da forma abaixo: 
- background#1.png
- background#2.png
- background#3.png
- background#4.png
- background#5.png
- background#6.png
- background#7.png
- background#8.png
- background#9.png

Após criar seus layers de cada camada vamos testar tudo.

- Abrir o PowerShell do Windows e Digitar: node index.js

Pronto, após rodar o comando seus NFTs estão criados na pasta "build".
Na pasta "imagens" se encontra as artes em NFT
Na pasta "json"se encontra todos os metadados (o DNA das NFTs)

Próxima aula:

Criação do IPFS no Pinata Clound
Como subir toda a coleção para o OpenSea de uma vez. 
