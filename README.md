# Arquitetura E-Commerce

Desenho de Solução para E-commerce utilizando Padrão C4 Model. 

O Objetivo desse desenho é mostrar a aplicabilidade da metodologia C4Model para um sistema de E-commerce, mostrar uma visao drilldown do projeto ou seja, de uma visão Macro até uma visão mais detalhada. 

O C4model determina 4 niveis de diagrama onde: 
 - Nivel 1 : System Context 
 - Nivel 2 : Container Context 
 - Nivel 3 : Component Context 
 - Nivel 4 : Code  
  
Utilizando o padrão C4model é possivel ter uma visão padronizada da solução.

** E-commerce: Nivel 1 - System Conxtext
![image](https://user-images.githubusercontent.com/3699130/151564304-64ce8628-3970-48aa-b0c2-75cf6f309849.png)  

Nesse nivel temos a visão da aplicação no contexto de sistema. Das integrações com sistemas externos ou fora de seu contexto. No caso do E-commercer seria a integração do Ecosistema do Ecommerce com serviços de terceiros, como por exemplo gate de pagamentos, sistemas de logistica, sistema de emissão de nota fiscal eletronica, integração com ERP e sistema de email marketing.  

** E-commerce: Nivel 2 -  Container Context
![image](https://user-images.githubusercontent.com/3699130/151567267-da9e3e6d-e2a7-42a9-a372-5b27c18779c0.png)

Nesse nível temos um zoom no nosso E-commerce apresentando uma visao um pouco mais detalhadas. Essa visão tem o objetivo de mostrar os grupos (containers) da solução. Trazendo visibilidade da sua segregação. 

** E-commerce: Nivel 3 - Component Context
![image](https://user-images.githubusercontent.com/3699130/151567739-4bbe38f4-4557-42f9-a5cd-32bf7e52f60e.png)

No nível Componente foi escolhido o Container API Application e dado um zoom para explorar com mais detalhes. Mostrar com um nível mais rico de detalhes suas integrações, seus componentes que trazem barreiras com o mundo externo e trazer todos os seus microserviços, bases de dados e afins. 

** E-commerce: Nivel 4 - Code  
Neste nivel é detalhada as jornadas do usuario em seus casos de usos. Para esse exemplo pegamos um cenário simples do usuario adicionando itens no carrinho 
![image](https://user-images.githubusercontent.com/3699130/151569580-1d1cb698-f639-4470-a18c-45b2ffe5e4b7.png)

A ideia desse Nível é o detalhamento maximo do componente, explirando todos as estorias de usuário para trazer riqueza e detalhamento para a documentação. Nem todos os processos são necessários chegar a esse nivel de detalhamento. Tudo depende do negocio e sua complexidade.  


Para uma visão da Topologia de infraestrura utilizada, foi criado o desenho abaixo o qual exemplifica os canais de comunicacao do cliente com o E-commerce. Os componentes que contralam a ligação da internet com seu meio Interno tanto na entrada de informação ou na integração com serviços terceiros. Tambem é apresentado uma arquitetura orientada a eventos. Esses eventos são disparados por seus microserviços e são publicados no Streamming Kafka. Esse Streamming é consumido inicialmente apenas para alimentar um Lake de dados para futuras implementações de Dashboards Analiticos. 
![image](https://user-images.githubusercontent.com/3699130/151570427-d85acaf8-2ba1-4181-aaf1-3223dd754d6f.png)



Referencia: www.c4model.com

