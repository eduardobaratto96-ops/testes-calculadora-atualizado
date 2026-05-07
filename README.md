ID da Falha: BUG-001
Título: [BUG] Campo de soma concatena texto em vez de somar números
Data / Hora: 06/05/2025 – 08:00
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: A função somar() pega os valores dos inputs como texto pois o tipo dos campos é type="text". Ao somar "2" + "2", o JavaScript concatena e retorna "22" em vez de 4.
Comportamento Esperado: O sistema deve converter os valores para número antes de operar e retornar 4.
Passos para Reproduzir:

Abrir o sistema
Digitar 2 no campo Número 1
Digitar 2 no campo Número 2
Clicar em Somar
Observar o resultado: exibe 22 em vez de 4
Evidências: Resultado exibido: 22. Correto seria: 4.


ID da Falha: BUG-002
Título: [BUG] Divisão por zero não é tratada – exibe Infinity
Data / Hora: 06/05/2025 – 08:05
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: A função dividir() não verifica se o segundo número é zero antes de dividir. O JavaScript retorna Infinity nesse caso.
Comportamento Esperado: O sistema deve exibir a mensagem "Não é possível dividir por zero!"
Passos para Reproduzir:

Digitar qualquer número no campo Número 1
Digitar 0 no campo Número 2
Clicar em Dividir
Observar que exibe Infinity
Evidências: Resultado exibido: Infinity. Deveria exibir mensagem de erro.


ID da Falha: BUG-003
Título: [BUG] Alert desnecessário aparece a cada operação matemática
Data / Hora: 06/05/2025 – 08:10
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: Todas as funções exibem um alert() após cada operação, interrompendo o fluxo do usuário.
Comportamento Esperado: O resultado deve ser exibido diretamente na tela sem interrupções.
Passos para Reproduzir:

Digitar dois números
Clicar em qualquer botão de operação
Observar que um alert aparece antes do resultado
Evidências: Alert com texto desnecessário bloqueia a interface a cada clique.


ID da Falha: BUG-004
Título: [BUG] Inputs preenchidos automaticamente com 212 após cada operação
Data / Hora: 06/05/2025 – 08:15
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: A função preencher Inputs Errados() sobrescreve os campos com o valor 212 após toda operação, sem o conhecimento do usuário.
Comportamento Esperado: Os campos devem permanecer com os valores digitados pelo usuário.
Passos para Reproduzir:

Digitar 5 e 3 nos campos
Clicar em Somar
Observar que os campos passam a exibir 212
Evidências: Campos alterados automaticamente para 212 sem ação do usuário.


ID da Falha: BUG-005
Título: [BUG] Campo de senha exibe o texto digitado em formato visível
Data / Hora: 06/05/2025 – 08:20
Reportado por: Eduardo Baratto – Equipe Front- end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O campo de senha usa type="text" em vez de type="password", expondo a senha digitada em texto visível na tela.
Comportamento Esperado: O campo deve usar type="password" para ocultar os caracteres digitados.
Passos para Reproduzir:

Acessar o formulário de cadastro
Digitar uma senha no campo Senha
Observar que os caracteres ficam visíveis
Evidências: Senha exibida em texto puro na tela.


ID da Falha: BUG-006
Título: [BUG] Confirmação de senha não verifica se as senhas coincidem
Data / Hora: 06/05/2025 – 08:25
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: A função cadastrar() não compara os campos senha e confirmar Senha. O cadastro é concluído mesmo com senhas diferentes.
Comportamento Esperado: O sistema deve bloquear o cadastro se as senhas forem diferentes.
Passos para Reproduzir:

Digitar senha1 no campo Senha
Digitar senha2 no campo Confirmar Senha
Clicar em Finalizar Cadastro
Observar que o cadastro é realizado mesmo assim
Evidências: Cadastro realizado com senhas diferentes sem nenhum aviso.


ID da Falha: BUG-007
Título: [BUG] Campo de e-mail aceita qualquer texto sem validação de formato
Data / Hora: 06/05/2025 – 08:30
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O campo de e-mail usa type="text" e não possui nenhuma validação. Qualquer texto é aceito como e-mail válido.
Comportamento Esperado: O campo deve exigir o formato correto (ex: usuario@dominio.com).
Passos para Reproduzir:

Digitar "texto qualquer" no campo Email
Clicar em Finalizar Cadastro
Observar que o cadastro é realizado normalmente
Evidências: Email inválido aceito sem nenhuma mensagem de erro.


ID da Falha: BUG-008
Título: [BUG] Alert automático a cada 15 segundos interrompe o usuário
Data / Hora: 06/05/2025 – 08:35
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O sistema usa setInterval para disparar um alert a cada 15 segundos, bloqueando completamente a interface.
Comportamento Esperado: Não deve haver nenhum alert automático disparado por intervalo de tempo.
Passos para Reproduzir:

Abrir o sistema
Aguardar 15 segundos
Observar que um alert aparece automaticamente
Evidências: Alert bloqueante disparado automaticamente sem ação do usuário.

ID da Falha: BUG-009
Título: [BUG] Campo CPF aceita qualquer texto sem validação de formato
Data / Hora: 06/05/2025 – 08:40
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O campo CPF usa type="text" e não possui nenhuma validação. Qualquer texto é aceito como CPF válido.
Comportamento Esperado: O campo deve validar o formato correto de CPF (ex: 000.000.000-00).
Passos para Reproduzir:

Digitar "abc" no campo CPF
Clicar em Finalizar Cadastro
Observar que o cadastro é realizado normalmente
Evidências: CPF inválido aceito sem nenhuma mensagem de erro.


ID da Falha: BUG-010
Título: [BUG] Campo telefone aceita qualquer texto sem limite de caracteres
Data / Hora: 06/05/2025 – 08:45
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O campo telefone usa type="text" sem nenhuma validação ou limite de caracteres, aceitando qualquer conteúdo.
Comportamento Esperado: O campo deve aceitar apenas números e respeitar o formato de telefone brasileiro.
Passos para Reproduzir:

Digitar "qualquer coisa aqui" no campo Telefone
Clicar em Finalizar Cadastro
Observar que o cadastro é realizado normalmente
Evidências: Telefone inválido aceito sem nenhuma mensagem de erro.


ID da Falha: BUG-011
Título: [BUG] Campo idade usa type="text" em vez de type="number"
Data / Hora: 06/05/2025 – 08:50
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O campo idade usa type="text", permitindo que o usuário digite letras ou símbolos no lugar de um número.
Comportamento Esperado: O campo deve usar type="number" e aceitar apenas valores numéricos positivos.
Passos para Reproduzir:

Digitar "vinte anos" no campo Idade
Clicar em Finalizar Cadastro
Observar que o cadastro é realizado normalmente
Evidências: Texto aceito no campo de idade sem nenhuma validação.


ID da Falha: BUG-012
Título: [BUG] Título da página muda automaticamente para "⚠ SISTEMA INSTÁVEL ⚠"
Data / Hora: 06/05/2025 – 08:55
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: Um setInterval altera o título da aba do navegador para "⚠ SISTEMA INSTÁVEL ⚠" a cada 3 segundos, causando confusão e transmitindo insegurança ao usuário.
Comportamento Esperado: O título da página deve permanecer fixo como definido no HTML.
Passos para Reproduzir:

Abrir o sistema
Aguardar 3 segundos
Observar que o título da aba muda automaticamente
Evidências: Título da aba alterado automaticamente sem ação do usuário.


ID da Falha: BUG-013
Título: [BUG] Variável "banana" declarada sem nenhum uso no código
Data / Hora: 06/05/2025 – 09:00
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O código contém a declaração let banana = 999999 sem nenhuma finalidade ou uso em qualquer parte do sistema. Código morto e desnecessário.
Comportamento Esperado: O código deve conter apenas variáveis e funções que sejam utilizadas.
Passos para Reproduzir:

Abrir o código-fonte do sistema
Localizar a linha let banana = 999999
Observar que a variável não é utilizada em nenhum lugar
Evidências: Variável declarada e nunca referenciada no código.


ID da Falha: BUG-014
Título: [BUG] Dados sensíveis do usuário exibidos no console.log após cadastro
Data / Hora: 06/05/2025 – 09:05
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: A função cadastrar() exibe no console do navegador todos os dados do usuário incluindo senha, CPF e email em texto puro, representando um sério risco de segurança.
Comportamento Esperado: Nenhum dado sensível deve ser exibido no console em ambiente de produção.
Passos para Reproduzir:

Preencher o formulário de cadastro
Clicar em Finalizar Cadastro
Abrir F12 e ir na aba Console
Observar que todos os dados incluindo senha aparecem expostos
Evidências: Senha e CPF exibidos em texto puro no console do navegador.


ID da Falha: BUG-015
Título: [BUG] Campos da calculadora usam type="text" em vez de type="number"
Data / Hora: 06/05/2025 – 09:10
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: Os campos num1 e num2 da calculadora usam type="text", permitindo que o usuário digite letras e símbolos no lugar de números.
Comportamento Esperado: Os campos devem usar type="number" para aceitar apenas valores numéricos.
Passos para Reproduzir:

Clicar no campo Número 1
Digitar "abc"
Observar que o campo aceita o texto normalmente
Evidências: Letras aceitas nos campos da calculadora sem nenhuma validação.


ID da Falha: BUG-016
Título: [BUG] Subtração e multiplicação não convertem texto para número
Data / Hora: 06/05/2025 – 09:15
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: As funções subtrair() e multiplicar() não usam parseFloat para converter os valores antes de operar, podendo retornar resultados incorretos dependendo do valor digitado.
Comportamento Esperado: Todas as funções devem converter os valores para número antes de realizar qualquer operação.
Passos para Reproduzir:

Digitar "5" no campo Número 1
Digitar "3" no campo Número 2
Clicar em Subtrair ou Multiplicar
Observar o resultado
Evidências: Operações realizadas sem conversão explícita de tipo.

ID da Falha: BUG-018
Título: [BUG] Campo nome aceita números e símbolos sem validação
Data / Hora: 06/05/2025 – 09:25
Reportado por: Eduardo Baratto – Equipe Front-end
Ambiente: Windows 11 – Google Chrome
Descrição da Falha: O campo nome não possui nenhuma validação de formato, aceitando números, símbolos e qualquer combinação de caracteres como nome válido.
Comportamento Esperado: O campo deve aceitar apenas letras e espaços, bloqueando números e símbolos.
Passos para Reproduzir:

Digitar "123!@#" no campo Nome
Clicar em Finalizar Cadastro
Observar que o cadastro é realizado normalmente
Evidências: Nome inválido aceito sem nenhuma mensagem de erro.


