# Sistema Bancário - Desafio 01

O código é dividido nas seguintes partes:

- **Declarações de importação:** O código importa o módulo textwrap para formatar o menu de opções.
- **Definição de funções:** O código define as seguintes funções:
    - menu(): Exibe um menu de opções para o usuário.
    - depositar(): Realiza um depósito em uma conta.
    - sacar(): Realiza um saque em uma conta.
    - exibir_extrato(): Exibe o extrato de uma conta.
    - criar_usuario(): Cria um novo usuário.
    - filtrar_usuario(): Filtra um usuário por CPF.
    - criar_conta(): Cria uma nova conta para um usuário.
    - listar_contas(): Lista todas as contas.
- **Corpo principal do programa:** O corpo principal do programa é um loop infinito que continua enquanto o usuário não selecionar a opção q (sair). O loop solicita ao usuário uma opção e, em seguida, chama a função correspondente.

O que faz cada função:

### **menu():**

A função menu() exibe um menu de opções para o usuário. O menu é formatado com o módulo textwrap para ficar mais legível.

### **depositar():**

A função depositar() realiza um depósito em uma conta. A função recebe o saldo atual da conta, o valor do depósito e o extrato da conta. A função verifica se o valor do depósito é maior que zero. Se for, o valor é adicionado ao saldo da conta e o extrato é atualizado com a operação de depósito.

### **sacar():**

A função sacar() realiza um saque em uma conta. A função recebe o saldo atual da conta, o valor do saque, o extrato da conta, o limite de saques e o número de saques já realizados. A função verifica se o valor do saque é maior que o saldo da conta, maior que o limite de saques ou excedeu o número máximo de saques. Se nenhuma dessas condições for atendida, o valor é subtraído do saldo da conta, o extrato é atualizado com a operação de saque e o número de saques é incrementado.

### **exibir_extrato():**

A função exibir_extrato() exibe o extrato de uma conta. A função recebe o saldo atual da conta e o extrato da conta. A função imprime o extrato formatado na tela.

### **criar_usuario():**

A função criar_usuario() cria um novo usuário. A função solicita ao usuário os dados do novo usuário (CPF, nome completo, data de nascimento e endereço). Os dados são então adicionados a uma lista de usuários.

### **filtrar_usuario():**

A função filtrar_usuario() filtra um usuário por CPF. A função recebe o CPF do usuário e uma lista de usuários. A função retorna o usuário da lista que corresponde ao CPF fornecido.

### **criar_conta():**

A função criar_conta() cria uma nova conta para um usuário. A função recebe a agência, o número da conta e uma lista de usuários. A função verifica se o CPF do usuário está na lista de usuários. Se estiver, a função cria uma nova conta com os dados fornecidos e a adiciona à lista de contas.

### **listar_contas():**

A função listar_contas() lista todas as contas. A função recebe uma lista de contas. A função imprime as informações de cada conta na tela.


### [Acesse o código aqui](/bootcamp_santander/python/01%20-%20Estrutura%20de%20dados/desafio.py)