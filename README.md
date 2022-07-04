### Group 8 (for week 2)

# Members

- Aimen Sahnoun
- Marshal Nganunu
- Celal Aksu
- Gabriel Horvart
- Ryan Chipwanya
- Inaki Cervera-Marzal


# Deployment

## 1- Vote contract deployment

RUNING SCRIPT:
`yarn ts-node ./scripts/1-deployVoteToken.ts`

CONTRACT ADDRESS  0x9E32540308BA6E517F42695456a366fA78fF2834
OUTPUT:

![vote_deploy_output](https://user-images.githubusercontent.com/32665644/176999758-4d828e1a-f717-4f94-bc0b-dac557371bc4.png)

Rinkeby etherscan screenshot:

![rinkeby_etherscan](https://user-images.githubusercontent.com/32665644/176999788-fc812ad7-237b-40ee-8837-ea834c9b9c1b.png)

## 2- CustomBallot.sol deployment

RUNING SCRIPT: 
`yarn ts-node ./scripts/2-deployCustomBallot.ts "Pizza" "Cake" "Hamburger" "Lasagna" "Popcorn" 0x9E32540308BA6E517F42695456a366fA78fF2834`

Input args:
Proposals: "Pizza" "Cake" "Hamburger" "Lasagna"

VoteToken Address: 0x9E32540308BA6E517F42695456a366fA78fF2834

CONTRACT ADDRESS  0xFCED99536D34c0fF0E33c999cF2F86c70BA53e7B
OUTPUT:

![customballotdeploy](https://user-images.githubusercontent.com/32665644/176999870-5feee462-5f43-464c-935c-b0a0ef507eda.png)

Rinkeby etherscan screenshot:

![rinkeby_etherscan](https://user-images.githubusercontent.com/32665644/176999888-79b64250-4f1e-4518-b56f-827c352a9c4e.png)

## 3- Mint MyToken Script

Runing script ( Script mints 10 MTK )

`yarn ts-node ./scripts/mintToken.ts 0x9E32540308BA6E517F42695456a366fA78fF2834 0x56491d3F87382b3fF39683B78b04457E06C40A89`

First Address is Token addres
Second address is mint to address

OUTPUT:

![mint_script](https://user-images.githubusercontent.com/32665644/176999979-58002628-89f0-4938-aeb8-7cc7ab35b32c.png)

Transaction:
https://rinkeby.etherscan.io/tx/0x5ab6f9928469a0b26806336f99523c9259d8339300294c75f28db99af5456326

Metamask:

![mint metamask](https://user-images.githubusercontent.com/32665644/177000040-3586a5a7-73c1-4d8f-8196-d3a60e923b45.png)

## 4- Delegate to self
Script is used in order to give voting power to self

**TOKEN Address used here: 0xb092E38cB079D2E6449F78a7CEDe1af14f0177cA
Ballot address used here : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D


RUNING SCRIPT: 
`yarn ts-node ./scripts/3-delegateToSelf 0xb092E38cB079D2E6449F78a7CEDe1af14f0177cA 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D`

Input args:
Token Address : 0xb092E38cB079D2E6449F78a7CEDe1af14f0177cA
Ballot Address : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D

Transaction  : 0x25814bd0f96f4c4704a168ba24e4d15c0cc3f7b4cc604dae59342214b30e87a8

## 5- Delegate to others


**TOKEN Address used here: 0xb092E38cB079D2E6449F78a7CEDe1af14f0177cA
Ballot address used here : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D


RUNING SCRIPT: 
`yarn ts-node ./scripts/4-delegateToOthers.ts <token address> <delegate-to>

Input args:
Token Address : 0xb092E38cB079D2E6449F78a7CEDe1af14f0177cA
Delegate To : 0x93da76CFc683E1536C91d37abcfE17a60c29B578

![delegate_to_other](https://user-images.githubusercontent.com/62159014/177184303-9faa0fb6-f216-4bd8-89b5-abdfd23edfed.png)


Transaction  : 0x73bde69a1d6f70e289acab817f3df5a48b0fc5c3bfe7323f9bbbc8ae2b08a258


## 6- Cast Vote



Ballot address used here : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D


RUNING SCRIPT: 
`yarn ts-node ./scripts/5-castVote.ts <ballot address> <proposal id> <voting amount>`

Input args:
Ballot Address : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D
Proposal ID :1
voting amount :5

![cast_vote](https://user-images.githubusercontent.com/62159014/177184637-ae3debdb-bbb3-442b-818d-e5daa50aeee8.png)



Transaction  : 


## 6- The Winning Proposal



Ballot address used here : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D


RUNING SCRIPT: 
`yarn ts-node --files scripts/6-winningProposal.ts <ballot address>`

Input args:
Ballot Address : 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D

Output :

$ /home/inaki/1-blockchain-projects/encodebootcamp/08-Tokenized-Votes/Project/node_modules/.bin/ts-node --files scripts/6-winningProposal.ts 0xF4A31a197a37d8472776336Da05AD8e58A6FA43D

Using address 0xc046cB6389571B43D09008828D6bC25e9997904E

[ '0xF4A31a197a37d8472776336Da05AD8e58A6FA43D' ]
The proposal with the most votes is Cake

Done in 3.47s.
