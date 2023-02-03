# Linux System Administrator - 703

## Laboratório 3 - Respostas


### 1) Abra o arquivo poesia.txt que está no diretório /root com o editor de textos VIM. Após isso, substitua todas as ocorrências da palavra misterio por segredo.

##### Resposta:
`:%s/misterio/segredo/g`


### 2) Copiar o trecho entre a linha 1 e 3 do arquivo poesia.txt.

##### Resposta:
`:1,3y`


### 3) Ativar a numeração de linhas do vim com o arquivo poesia.txt aberto.

##### Resposta:
`:set nu`


### 4) Ativar o modo sintax no vim com o arquivo poesia.txt aberto.

##### Resposta:
`:syntax on`


### 5) Pesquisar a palavra “sol” no vim com o arquivo poesia2.txt aberto.

##### Resposta:
`/sol`


### 6) Destacar palavras pesquisadas no VIM com o arquivo poesia.txt aberto.

##### Resposta:
`:set hlsearch`


### 7) Com o arquivo poesia.txt aberto no VIM, salve o arquivo sem sair do VIM.

##### Resposta:
`:w`


### 8) Com o arquivo poesia.txt aberto no VIM salve forçadamente este arquivo com o mesmo nome só que no diretório /tmp.

##### Resposta:
`:w! /tmp/poesia2.txt`


### 9) Execute o comando ls no VIM  com o arquivo poesia2.txt aberto.

##### Resposta:
`:!ls`


### 10) Com o arquivo poesia2.txt aberto, sair sem gravar do editor VIM.

##### Resposta:
`:q`
