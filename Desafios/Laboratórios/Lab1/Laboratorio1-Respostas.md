# Linux System Administrator - 703

## Laboratório 1 - Respostas


### 1) Execute o comando ls usando o caminho absoluto.

##### Resposta: 
`/bin/ls`


### 2) Visualize o conteúdo da variável $HOME.

##### Resposta:
`echo $HOME`

### 3) Acesse o diretório que armazena a documentação do Linux.

##### Resposta:
`cd /usr/share/doc`


### 4) Visualize os 10 últimos comandos no histórico do usuário root.

##### Resposta:
`fc -l 10`
ou
`history | tail`
ou
`history | tail -n 10`

### 5) Crie um diretório chamado arquivos em /tmp usando caminho absoluto tomando cuidado para não sobrescrever o diretório caso o mesmo já existir.

##### Resposta:
`mkdir -p /tmp/arquivos`


### 6) Visualize as 5 últimas linhas do arquivo /etc/passwd usando caminho absoluto.

##### Resposta:
`tail -n 5 /etc/passwd`

### 7) Usando o comando awk mostre uma lista de logins de usuários com UID maior que 999.

##### Resposta:
`awk -F: '($3 > 999) {print $1}' /etc/passwd`

### 8) Mostre na saída padrão o conteúdo do arquivo /etc/passwd em letras maiúsculas.

`tr [a-z] [A-Z] < /etc/passwd`

### 9) Use o comando que mostra quantas linhas possui o arquivo /etc/passwd usando o caminho absoluto.

##### Resposta:
`wc -l /etc/passwd`

### 10) Com um só comando tente ler todo o conteúdo do diretório (arquivos e pastas) /etc encaminhando a saída normal para o /dev/null e a saída de erros também. Lembre-se o comando cat lê somente arquivos de textos e quando é executado passando como parâmetro um diretório é gerada uma saída de erro.

##### Resposta:
`cat /etc/* > /dev/null 2>&1`

