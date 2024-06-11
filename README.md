# Nexus_Testes
Testes do nosso projeto Nexus



 Teste 1: Login com Credenciais Válidas

Feature: Login

  Scenario: Login com Credenciais Válidas
  
    Given o usuário está na página de login
    
    When o usuário insere um email válido
    
    And o usuário insere uma senha válida
    
    And o usuário clica no botão "Login"
    
    Then o usuário deve ser redirecionado para a página inicial
    
    And uma mensagem de boas-vindas deve ser exibida



Teste 2: Login com Email Inválido

Feature: Login

  Scenario: Login com Email Inválido
  
    Given o usuário está na página de login
    
    When o usuário insere um email não cadastrado
    
    And o usuário insere uma senha qualquer
    
    And o usuário clica no botão "Login"
    
    Then uma mensagem de erro "Email ou senha incorretos" deve ser exibida





Teste 3: Login com Senha Incorreta



Feature: Login

  Scenario: Login com Senha Incorreta
  
    Given o usuário está na página de login
    
    When o usuário insere um email válido
    
    And o usuário insere uma senha incorreta
    
    And o usuário clica no botão "Login"
    
    Then uma mensagem de erro "Email ou senha incorretos" deve ser exibida





  Teste 4: Login com Campos Vazios

  Feature: Login

  Scenario: Login com Campos Vazios
  
    Given o usuário está na página de login
    
    When o usuário deixa os campos de email e senha vazios
    
    And o usuário clica no botão "Login"
    
    Then mensagens de validação devem ser exibidas indicando que ambos os campos são obrigatórios




  Teste 5: Login com Email em Formato Inválido

  Feature: Login
  
  Scenario: Login com Email em Formato Inválido
  
    Given o usuário está na página de login
    
    When o usuário insere um email em formato inválido
    
    And o usuário insere uma senha qualquer
    
    And o usuário clica no botão "Login"
    
    Then uma mensagem de erro "Formato de email inválido" deve ser exibida


Teste 6: Login com Senha de Menos de 6 Caracteres

Feature: Login

  Scenario: Login com Senha de Menos de 6 Caracteres
  
    Given o usuário está na página de login
    
    When o usuário insere um email válido
    
    And o usuário insere uma senha com menos de 6 caracteres
    
    And o usuário clica no botão "Login"
    
    Then uma mensagem de erro "A senha deve ter pelo menos 6 caracteres" deve ser exibida

Teste 7: Login com Espaços em Branco no Email

Feature: Login

  Scenario: Login com Espaços em Branco no Email
  
    Given o usuário está na página de login
    
    When o usuário insere um email válido com espaços em branco antes ou depois
    
    And o usuário insere uma senha válida
    
    And o usuário clica no botão "Login"
    
    Then o sistema deve ignorar os espaços em branco e permitir o login se as credenciais forem válidas


Teste 8: Login com Senha em Branco

Feature: Login

  Scenario: Login com Senha em Branco
  
    Given o usuário está na página de login
    
    When o usuário insere um email válido
    
    And o usuário deixa o campo de senha vazio
    
    And o usuário clica no botão "Login"
    
    Then uma mensagem de erro "A senha é obrigatória" deve ser exibida



  Teste 9: Login com Email e Senha Corretos, Mas Conta Não Verificada

  Feature: Login

  Scenario: Login com Email e Senha Corretos, Mas Conta Não Verificada
  
    Given o usuário está na página de login
    
    When o usuário insere um email válido
    
    And o usuário insere uma senha válida
    
    And o usuário clica no botão "Login"
    
    Then uma mensagem deve ser exibida informando que a conta não foi verificada e solicitando a verificação do email


Teste 10: Logout Após Login


Feature: Login

  Scenario: Logout Após Login
  
    Given o usuário está logado
    
    When o usuário navega até a opção de logout
    
    And o usuário clica em "Logout"
    
    Then o usuário deve ser redirecionado para a página de login
    
    And uma mensagem "Logout realizado com sucesso" deve ser exibida

   





