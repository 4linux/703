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
