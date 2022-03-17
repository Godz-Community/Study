Como criar SUA COLEÇÃO DE NFT sem SABER PROGRAMAÇÃO (By MultMcGame#8099)

PARTE III

Nas aulas anteriores nosso foco como dito foi em ERC1155

ERC1155 geralmente o mesmo usado em games NFTs na BSC e MATIC, o mint e bem mais barato pelo motivo de se poder mintar em lotes por um valor bem barato.
Agora vamos estudar a cereja do bolo que é o ERC721 onde é usado frequentemente na rede ETH, com valor de preço no contrato e botãozinho direto no site para o mint.
Lembrando que no ERC721 o mint é unitário por isso seu valor é bem elevado em comparação ao anterior.

Leia as aulas anteriores...

Programas Usados para criação de NFTs!

Sublime (sublime_text_build_4126_x64_setup)
Node JS (node-v16.14.0-x64)
PowerShell do Windows
Visual Studio Code (VSCodeUserSetup-x64-1.64.2)
Arquivo Botão para site + Contrato (https://drive.google.com/file/d/1OaMaW88jPIa62FqLpDEPP1siEdlAOe2w/view?usp=sharing)

Os procedimentos de criação do NFT é o mesmo anterior até o pornto de criação da CID (por isso pedi para voltar e ler)

- Vá no site: https://remix.ethereum.org/
- Em baixo de default_wordspace vai ter um desenho de uma caderno, coloque o mouse em cima (create new file)
- coloque o nome do seu projeto ou a abreviação ex: BOREDAPE.sol (não esqueça do sol)
- Selecione na sua sua metamask a rede de criação da coleção das suas NFTs.(ETH)

- Abra o arquivo contrato, copie tudo e cole no espaço vazio criado anteriormente no remix

Daqui para frente iremos usar a metamask, lembrando que precisamos de muita segurança nesta hora.
Esteja com um endereço de metamask nova
Nunca use este endereço misturado com jogos NFTs e jamais conecte este endereço em sites desconhecidos.
Guarde suas seed em local seguro e se possível use uma trezor 
Nesta parte do contrato:

- Na linha 09 em "ZBabys"mude para o nome que desejar, pode ser ex: contrato
- Na linha 13 em  uint256 public mintRate = 0.005 ether; defina o valor que você deseja verder suas NFTs
- Na linha 14 em  uint public MAX_SUPPLY = 10000; defina o supply da sua coleção
- Na linha 16 em  constructor() ERC721("ZBabys", "ZBABYS") {} defina o nome do seu projeto e o símbolo da moeda
- Na linha 18 a 24 encontra-se a função do SAFE mint (BOTÃO) Caso ainda tenha NFTs disponíveis baseado no supply ele irá funcionar, e vai dar uma mensagem de erro caso as NFTs tenham acabado.

Das linhas 25 a 29 você pode configurar a divisão das vendas caso queira, lembrando que todas tem que somar o valor definido na linha 13
Caso não ache necessário pode apagar, Ficando ao seu cargo:

address payable marketing = payable(0xbE94ea17dEb769d28E892298C5c611AebF08F5F8);
address payable development = payable(0x9238BEE019c8B7EdB30322B804D62363F912c5fC);
marketing.transfer(0.001 ether);
development.transfer(0.001 ether);
// marketing.transfer(msg.value/100); if porcentagem 1%

- Na linha 33 substitua IPFS pelo a da sua coleção.

A função URI é usada como proteção anti hacker, evitando de pessoas usarem o seu "json"para clonar o seu projeto.

E ao final:
Na linha 54 teremos a função de withdraw onde o valor da venda não vai para a sua carteira e sim para o contrato.
Onde somente o dono do contrato pode efetuar o saque "onlyOwner"
Mais uma segurança...

- Clique em solidity compiler e copile, se der verde (check) esta tudo OK
- No campo account vai seu endereço de metamask
- No campo Contract selecione o nome do seu contrato (linha 9) 
- Clique em deploy mude o JavaScript VM para Injected Web3

Vai cobrar a taxa da criação do contrato.
Ele vai ler sua metamask na rede que esta conectada (ETH) é onde sera feito o deploy

- Não feche o remis ainda!

VAMOS AO BOTÃO

- Entre na pasta data e abra o arquivo contract.JSON
{
    "contract": {

        "abi" : , // CÓDIGO ABI DO CONTRATO
    "address" : [ {"address": "0x00000000000000000000000"} ], // ENDEREÇO DO SEU CONTRATO
    "confGas" : [ {"gaslimit": "3000000"} ], // PREÇO DO GÁS
    "coust" : [ {"amount" : "0.005"} ] // VALOR QUE DESEJA VENDER CADA 1 NFT

    }
}

- Volte no remix no botão de check
- Em contract selecione o contrato que acabou de criar
- Embaixo vai ter um botão chamado ABI (sopie ele)
- Volte no codigo do botão botão.

- Na linha 04 cole a sua ABI antes da virgula e apague todos os campos vendes de referência.
- Na linha 05 substitua o 0x00000000000000000000000 pelo endereço do seu contrato.
- Na linha 06 caso for rede de test deixe 2100000, caso for na rede normal deixe 2100000
- Na linha 07 repita o valor exato da sua NFT setado no contrato
- Salve

Basta jogar na pasta da sua hospedagem, onde fica seu INDEX do seu site.
Pode ficar a vontade para mudar o CSS ao seu gosto, deixei um simples.

A função de saque pode ser feito em white contract ou pelo botão do seu site.

É isso pessoal, façam bastante teste pela testnet e fiquem fera.

E lembrando se vcs ficarem ricos lembre de mim!
