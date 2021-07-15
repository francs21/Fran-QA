# Fran-QA
Casos de Teste - Compras no e-commerce Sauce.
--------------------------------------------------

Neste documento estão descritos os pré-requisitos, todos os casos de testes e
passo a passo para a validação dos mesmos.
___________________________________________________________________________________________________________________________________________________________

Pré-requisito para execução de testes:
----
1. Ter um aparelho com acesso à internet
___________________________________________________________________________________________________________________________________________________________

Casos de Teste
--------

1.	Validar acesso ao e-commerce.
--------------------------------------------------------------------------------------
Step 1: Digitar o URL: <https://www.saucedemo.com> no navegador.

Expect Result: O sistema deverá ser exibir a tela de login que dará acesso ao e-commerce.

Step 2: Inserir dados de usuário no campo “Username”, senha no campo “Password”  válidos e clicar em “login”
 
Expect Result: O sistema deverá permitir o acesso ao site, direcionando o usuário para a tela inicial “PRODUCTS” exibindo os produtos em ordem original.

___________________________________________________________________________________________________________________________________________________________
2.	Validar a ordenação de produtos através da opção de exibição “PRICE (low to high)”
----------------------------------------------------------------------------------------------

Step 1: Clicar no ícone de filtro, localizado no canto superior esquerdo da página inicial.

Expect Result: O sistema deverá expandir com as opções de ordenação para visualização de produtos.

Step 2: Selecionar a opção “PRICE (low to high)”

Expect Result: O sistema deverá ordenar a exibição de produtos com preço do menor para o maior, sendo exibidos da esquerda para a direita.
 
___________________________________________________________________________________________________________________________________________________________
3.	Validar adição dos produtos “Sauce Labs Onesie” e “Test.allTheThings() T-Shirt (Red)” ao carrinho.
------------------------------------------------------------------------------------------------------------
Step 1: Localizar o produto “Sauce Labs Onesie” e clicar no botão “ADD TO CARD”

Expect Result: O botão “ADD TO CART” deverá alterar para “REMOVE” e o ícone do carrinho deverá ser exibido com a contagem de produtos adicionados.

Step 2: Localizar o produto “Test.allTheThings() T-Shirt (Red)” e clicar no botão “ADD TO CARD”

Expect Result: O botão “ADD TO CART” deverá alterar para “REMOVE” e o ícone do carrinho deverá ser exibido com a contagem de produtos adicionados.

Obs.: Confirmar nome do produto “Test.allTheThings() T-Shirt (Red)” com Dev antes de validar o teste.

___________________________________________________________________________________________________________________________________________________________
4.	Validar acesso ao carrinho
---------------------------------------------------------------------------------------------------------
Step 1: Clicar no ícone do carrinho 
                              
Expect Result: O sistema deverá exibir a tela com título “YOUR CART” e com os produtos adicionados ao carrinho anteriormente.
 
___________________________________________________________________________________________________________________________________________________________
5.	Validar funcionalidade do botão “REMOVE” (teste de falha)
-------------------------------------------------------------------------------------------------------
Step 1: Clicar no botão “REMOVE” de um produto do carrinho.

Expect Result: O produto deverá ser removido do carrinho, a contagem do ícone deverá diminuir de acordo com quantidade de produtos existentes no carrinho.
 
___________________________________________________________________________________________________________________________________________________________
6.	Validar funcionalidade do botão “CONTINUE SHOPPING” (teste de falha)
-------------------------------------------------------------------------------------------------------------
Step 1: Clicar no botão “CONTINUE SHOPPING” localizado no canto inferior esquerdo da tela.

Expect Result: O Sistema deverá retornar para a tela inicial exibindo todos os produtos, na ordem original do sistema.

___________________________________________________________________________________________________________________________________________________________
7.	Validar conclusão da compra
---------------------------------------------------------------------------------------------------------------------
Step 1: Na tela do carrinho, clicar no botão “CHEKOUT” localizado no canto inferior direito

Expect Result: O Sistema irá direcionar para a tela “CHEKOUT: YOUR INFORMATION” 

Step 2: Preencher o campo “First Name” com o primeiro nome do usuário, o campo “Last Name” com o último nome do usuário, o campo “Zip/Postal Code” com o CEP do endereço do usuário e clicar no botão “CONTINUE”

Expect Result: O Sistema irá direcionar para a tela “CHEKOUT: OVERVIEW” 
com os produtos inseridos no carrinho, informações da compra com os campos “Payment Information:”, “Shipping Information:”, valor total da compra, valor da taxa, valor total com valor da compra + taxa e os botões “CANCEL” e “FINISH” no inferior da tela.
 
Step 3: Clicar no botão “FINISH” 

Expect Result: O Sistema irá direcionar para a tela “CHEKOUT: COMPLETE!”, exibindo a mensagem de título “THANK YOU FOR YOUR ORDER”, corpo “Your order has been dispatched, and will arrive just as fast as the pony can get there!”, uma imagem “SAUCE LABS” e botão “BACK HOME”
 
Step 4: Clicar no botão “BACK HOME” 

Expect Result: O Sistema irá direcionar para a tela inicial do e-commerce “PRODUCTS”, exibindo todos os produtos em ordem original e ícone do carrinho com a contagem zerada.

___________________________________________________________________________________________________________________________________________________________
8.	Validar funcionalidade do botão “CANCEL” da tela “CHEKOUT: YOUR INFORMATION” (teste de falha)
----------------------------------------------------------------------------------------------------------------------------------------
Step 1: Após inserir os dados solicitados na tela, clicar no botão “CANCEL” localizado no canto inferior esquerdo da tela.
 
Expect Result: O sistema deverá retornar para a tela do carrinho “YOUR CART”

___________________________________________________________________________________________________________________________________________________________
9.	Validar funcionalidade do botão “CANCEL” da tela “CHEKOUT: OVERVIEW” (teste de falha)
-------------------------------------------------------------------------------------------------------------------------------------------
Step 1: Após inserir os dados solicitados na tela, clicar no botão “CANCEL” localizado no canto inferior esquerdo da tela.
 
Expect Result: O sistema deverá retornar para a tela inicial “PRODUCTS” exibindo os produtos na ordem original e ícone de carrinho com contagem de produtos já inseridos.

 





