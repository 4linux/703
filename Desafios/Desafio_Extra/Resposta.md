# **Desafio**

## **Cenário:**

### **Objetivo:** Sua tarefa é criar os usuários de sistema para os funcionários da empresa **BOOKSTORE** e os diretórios (pastas) para estes usuários ajustando as permissões para que apenas os usuários do grupo tenham acesso apenas aos arquivos de sua determinada área.


## **Grupos:**


### **Diretoria:**
|**Nome**|**Login**|
| - | - |
|Leonardo Amorim|leonardoamorim|
|Cesar Domingos|cesardomingos|



### **Gerência:**
|**Nome**|**Login**|
| - | - |
|João Silva|joaosilva|
|Ana Maria|anamaria|



### **Logística:**
|**Nome**|**Login**|
| - | - |
|Marcelo Pereira|marcelopereira|
|Antônio da Costa|antoniocosta|
|Mariana Campos|marianacampos|
|Cláudia da Silva|claudiasilva|
|Vitor Hugo|vitorhugo|
|Pedro Henrique|pedrohenrique|



### **Departamento de TI:**
|**Nome**|**Login**|
| - | - |
|Ricardo Pereira|ricardopereira|
|Thiago Santos|thiagosantos|
|Marcela Pinheiro|marcelapinheiro|
|Ana Júlia|anajulia|
|José Oliveira|joseoliveira|
|Francisco Hitao|franciscohitao|


## **Regras para criação e permissões das pastas:**

- Criar todos os usuários do organograma;
- Para facilitar defina a senha de todos os usuários como 123456;
- Criar os grupos diretoria, gerencia, logistica e ti;
- Inserir os usuários em seus respectivos grupos de acordo com o organograma;
- Criar as pastas diretoria, gerencia, logistica e ti em /mnt;
- O dono de todos os diretórios será o root e o grupo será o respectivo departamento;
- A diretoria pode acessar qualquer pasta (leitura e escrita);
- Os outros departamentos só podem acessar suas respectivas pastas;
- Deve existir um mecanismo para evitar que um usuário de um mesmo grupo remova arquivo que outro usuário criou;
- Os arquivos criados dentro destas pastas devem clonar dono e grupo da pasta para que os arquivos também sejam do grupo;
- O funcionário Francisco Hitao deverá ter seu login bloqueado por estar afastado da empresa;
- O funcionário Vitor Hugo está com sua conta bloqueada e deverá ser desbloqueada;
- Crie um grupo chamado shutdown para inserir usuários que possam desligar a máquina;
- O funcionário Thiago Santos deverá ter permissão para desligar o computador;
- O diretores Leonardo Amorim e Cesar Domingos solicitaram a geração de uma senha segura com o comando dd para que ele memorizasse;
- Não esquecer de fazer um check-list para verificar se os usuários foram realmente criados, se as permissões e donos das pastas estão corretos.



# **Solução do exercício:**

### **Criando as pastas:**

\# mkdir -p /mnt/diretoria

\# mkdir -p /mnt/gerencia

\# mkdir -p /mnt/logistica

\# mkdir -p /mnt/ti

### **Criando os usuários:**

\# adduser leonardoamorim

\# adduser cesardomingos

\# adduser joaosilva

\# adduser anamaria

\# adduser marcelopereira

\# adduser antoniocosta

\# adduser marianacampos

\# adduser claudiasilva

\# adduser vitorhugo

\# adduser pedrohenrique

\# adduser ricardopereira

\# adduser thiagosantos

\# adduser marcelapinheiro

\# adduser anajulia

\# adduser joseoliveira

\# adduser franciscohitao

### **Criando os grupos:**

\# groupadd diretoria

\# groupadd gerencia

\# groupadd logistica

\# groupadd ti

### **Inserindo os usuários em seus respectivos grupos:**

\# gpasswd -a leonardoamorim diretoria

\# gpasswd -a cesardomingos diretoria

\# gpasswd -a joaosilva gerencia

\# gpasswd -a anamaria gerencia

\# gpasswd -a marcelopereira logistica

\# gpasswd -a antoniocosta logistica

\# gpasswd -a marianacampos logistica

\# gpasswd -a claudiasilva logistica

\# gpasswd -a vitorhugo logistica

\# gpasswd -a pedrohenrique logistica

\# gpasswd -a ricardopereira ti

\# gpasswd -a thiagosantos ti

\# gpasswd -a marcelapinheiro ti

\# gpasswd -a anajulia ti

\# gpasswd -a joseoliveira ti

\# gpasswd -a franciscohitao ti


### **Ajustando dono e grupo de cada pasta:**

\# chown root.diretoria /mnt/diretoria

\# chown root.gerencia /mnt/gerencia

\# chown root.logistica /mnt/logistica

\# chown root.ti /mnt/ti

### **Ajustando as permissões:**

\# chmod 3770 /mnt/diretoria

\# chmod 3770 /mnt/gerencia

\# chmod 3770 /mnt/logistica

\# chmod 3770 /mnt/ti

\# gpasswd -a leonardoamorim gerencia

\# gpasswd -a cesardomingos gerencia

\# gpasswd -a leonardoamorim logistica

\# gpasswd -a cesardomingos logistica

\# gpasswd -a leonardoamorim ti

\# gpasswd -a cesardomingos ti

\# groupadd shutdown

\# chown root.shutdown /sbin/shutdown

\# gpasswd -a thiagosantos shutdown

\# chmod 4775 /sbin/shutdown

\# ln -s /sbin/shutdown /bin/shutdown

### **Bloquear o usuário Francisco Hitao:**

\# passwd -l franciscohitao

ou

\# usermod -L linustorvalds


### **Desbloquear o usuário Vitor Hugo:**

\# passwd -u vitorhugo

ou

\# usermod -U vitorhugo

## **Fazer check-list:**

### **Verificar se os usuários foram criados:**

\# cat /etc/passwd | grep <login-do-usuario>

### **Verificar se os grupos foram criados:**

\# cat /etc/group | grep <nome-do-grupo>

### **Verificar se o usuário está em um grupo:**

\# groups <usuario>

### **Verificar as permissões:**

\# ls -dl /mnt/diretoria

\# ls -dl /mnt/gerencia

\# ls -dl /mnt/logistica

\# ls -dl /mnt/ti

> Se não retornar nada, significa que o usuário ou grupo não foi criado ou está com outro nome.

### **Verificar se o usuário Francisco Hitao realmente está bloqueado:**

\# cat /etc/shadow | grep franciscohitao

