# Linux System Administrator - 703

## Laboratório 4 - Respostas


### 1) Dividir arquivo.tar cada parte terá com 5MB.

##### Resposta:
`split -b 5M arquivo.tar` 


### 2) Gere um arquivo a.txt em /tmp com NUL de 1MB.

##### Resposta:
`dd if=/dev/zero of=/tmp/a.txt count=1024 bs=1024`


### 3) Veja o tamanho do arquivo /tmp/a.txt.

##### Resposta:
`du -h /tmp/a.txt` 
ou
`ls -lh /tmp/a.txt `


### 4) Veja quantos caracteres tem o /etc/passwd.

##### Resposta:
`wc -c /etc/passwd`


### 5) Crie a base de dados para o locate.

##### Resposta:
`updatedb`


### 6) Busque no diretório raiz apenas arquivos vazios.

##### Resposta:
`find / -type f -empty`


### 7) Busque no diretório raiz apenas diretórios vazios.

##### Resposta:
`find / -type d -empty`


### 8) Busque todos arquivos com permissão 777.

##### Resposta:
`find / -type f -perm 777`


### 9) Busque todos arquivos maiores que 10M.

##### Resposta:
`find / -size +10M`


### 10) Busque todos arquivos modificados 20 dias atrás.

##### Resposta:
`find / -mtime 20`

