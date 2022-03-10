# Como criar SUA COLEÇÃO DE NFT sem SABER PROGRAMAÇÃO (By MultMcGame#8099)

## PARTE II

Lembretes importantes:

Tente usar nomes sempre em inglês e com a primeira letra em caixa alta
Sempre substitua também por_ os espaços do nome das camadas ex: Blue_Hat#9.png (caso não faça isso o código ira dar erro quando for gerar as NFTs)
Quanto mais for o número mais comum é a NFT.
Uma opção caso não queira que sua NFT não tenha uma acessório basta fazer a camada totalmente transparente e renomear ela como ex: Blue_Hat#10.png
Nas subpastas da pasta "layers" nunca as deixe vazias, sempre delete as que não irão usar (caso não faça isso o código ira dar erro quando for gerar as NFTs)

Lembram desta ordem? Pois é, ele foi só um exemplo, mas aqui vou tentar explicar melhor.
Lá no seu editor de imagens temos as camadas e aqui funciona da mesma forma. voltando lá no sublime no arquivo config iremos fazer da forma como criamos as camadas no editor de imagem, uma sobreposta corretamente sobre a outra.

Exemplo errado:
```
 layersOrder: [
      { name: "Accessories" },
      { name: "Background" },
      { name: "Clothing" },
      { name: "Body" },
      { name: "Earring" },
```
Exemplo correto:
```
 layersOrder: [
      { name: "Background" },
      { name: "Body" },
      { name: "Clothing" },
      { name: "Earring" },
      { name: "Accessories" },
```
Sempre usamos primeiro fundo, depois corpo e depois vem os demais acessórios, não erre nisso. Ok, 
Voltando...

- Faça o procedimento anterior e crie 10 NFTs
- Entrar no https://www.pinata.cloud/
- Criar a conta (conta free tem 1 GB de arquivo, caso sua coleção seja maior ae tem que pagar)
- Clicar em upload
- Folder
- Select
- Selecione a pasta C:\hashlips\build\images

- Colocar em name: IPFS_IMAGES
- Clique em upload

Ele vai fazer o upload dos arquivos e após o upload ele vai criar uma CID que é o seu IPFS.

- Copie ele e volte no sublime e substitua a IPFS por este e salve
- No PowerShell do Windows na pasta hashlips digite: "node" de um espaço aperte a letra U depois TAB do seu teclado para ele entrar na pasta utils
- depois aperte a letra U novamente e depois o TAB ficando assim: node utils/updade_info.js
- Aperte Enter

Pronto agora seus arquivos de metadados foram substituídos pelo IPFS de vocês. (pode verificar que no metadados já não existe o meu IPFS mais)

- Faça o upload da pasta "json" para o PINATA com seu IFS atualizado.
- Colocar em name: IPFS_JSON
- Clique em upload

Agora você vera duas CID onde:
Uma é das imagens e a outra é dos metadados.

- Vá no site: https://remix.ethereum.org/
- Em baixo de default_wordspace vai ter um desenho de uma caderno, coloque o mouse em cima (create new file)
- coloque o nome do seu projeto ou a abreviação ex: BOREDAPE.sol (não esqueça do sol)
- Selecione na sua sua metamask a rede de criação da coleção das suas NFTs.

Lembre que este manual é para a mintagem direta, portanto caso escolha rede ETH, fique ciente que você ira pagar a mintagem de acordo com o número de NFTs que você criou.
Aconselho usar este manual somente para mintagem de NFT na rede MATIC (Que é bem barato)
Posteriormente irei postar outros manuais mais avançados onde os compradores é que dão Mint nas NFTs.

- Abra o arquivo contrato, copie tudo e cole no espaço vazio criado anteriormente no remix

Caso tenha dúvida ou caso queira aprender sobre contratos vá no [github oficial do OpenZeppelin](https://github.com/OpenZeppelin).
Daqui para frente iremos usar a metamask, lembrando que precisamos de muita segurança nesta hora.
Esteja com um endereço de metamask nova
Nunca use este endereço misturado com jogos NFTs e jamais conecte este endereço em sites desconhecidos.
Guarde suas seed em local seguro e se possível use uma trezor

Nesta parte do contrato:

Na linha "maxSupply" coloque a quantidade das suas NFTs, pode colocar a mais caso for criar mais posteriormente ou pode apagar
Na linha "maxMintAmount" coloque a quantidade das suas NFTs
Na linha "constructor" coloque sua CID do metadados feito no Pinata
Na linha "name = coloque o Nome da coleção
Na linha "symbol" coloque o Simbolo da sua NFT
Na linha "return"  coloque sua CID do metadados feito no Pinata

- Clique em solidity compiler e copile, se der verde (check) esta tudo OK
- Clique em deploy mude o JavaScript VM para Injected Web3

Ele vai ler sua metamask e na rede que esta conectada é onde sera feito o deploy

- selecione a carteira e deixe o saldo da mintagem

Geralmente o mint de cerca de 50 NFTs não passa de 0.5 MATIC

- Copie o código do contrato criado. SALVE!!!

- Vá no opensea: https://opensea.io/get-listed
- selecione a rede (geralmente é live on a mainnet)
- selecione a rede ETH ou MATIC de criação anterior
- coloque o seu contrato
- submit

Pronto sua coleção esta criada! Com metadados e tudo mais....TOP heim! Venda e envie para os amigos!
Qualquer outro market pode ser listados seus NFTs porque nesse manual ensinei vocês a fazer por contrato. 
O dia que vcs ficarem RICOS lembrem de mim ae heim! 💰
Este manual é para NFTs ERC1155 o próximo farei do ERC721
