# Chatbot-Watson

Segue no link abaixo prévia do Chatbot Watson desenvolvido para clientes que querem montar uma refeição no restaurante FIT & Meals com opções de protéina, e ainda escolher o ponto da carne vermelha. No cardápio é possível escolher opções de legumes e arroz(normal ou integral) e concomitantemente tirar dúvidas sobre os alimentos.
Ao finalizar o pedido o assistente virtual confirma novamente o pedido e simula a transação financeira, pedindo ao usuário para inserir email. Inserido o email o assistente confirma o envio do email e passa número de telefone do restaurante FIT & Meals em caso de dúvida.

## https://assistant-chat-us-south.watsonplatform.net/web/public/f35cac3b-aeff-4eb4-a0e5-e75ded92ddda

O presente projeto é apenas uma prévia do assistente virtual. Sobre a construção do fluxo foi baseado em desambiguação e num conceito de fluxo fechado, onde o usuário tem no máximo 2 opções de rota para evitar que o assistente dê um resposta errada ou perca o sentido, ou até mesmo num cenário real o cliente não opte pela compra. Foram feitos **slotes** para cada tipo de comida, em formato sequêncial simulando um formato de Menu para o usuário. A seleção é feita unidirecional e é requirido que o usuário digite algo para seguir.
Na sequência de dúvidas(benefícios) sobre os alimentos, o fluxo seguiu com mesmo formato, porém com opção do usuário sair de cada **Slot** digitando "não" até sanar todas dúvidas. 

# Fluxo Dialog

![Dialog watson](https://user-images.githubusercontent.com/51059036/70104775-dfa1b180-161d-11ea-9d18-2352192de57c.PNG)

# Digressions

Nesse ponto usamos o conceito de **Digressions**, onde o usuário pode entrar em sair de um fluxo sem perder a sequência da comunicação. Como exemplo, nesse chatbot se o usuário estiver montando sua refeição e perguntar sobre os benefícios de um alimento, o assistente irá dar a informação sobre o alimento e retonar ao fluxo de montar o cardápio. Ao tirar uma dúvida adicionei a mensagem "Me conte mais sobre sua dúvida ou vamos montar seu prato!" e logo em seguida restaura o fluxo de montagem de pedido, como forma de captar a venda. Há a opção também de continuar tirando dúvidas e mesmo assim voltamos para o fluxo da venda(montagem do pedido) a cada vez (**skip to response**).

![duvida1](https://user-images.githubusercontent.com/51059036/70105749-7d967b80-1620-11ea-9b91-a590b68268e7.PNG)

# Próximos Steps

Acessar git IBM Assistent sample(git clone), NPM install para instalar as dependências do projeto. Passar as credênciais API para startar o assistente. 
NPM start - para iniciar o Assistente. Primeiramente podemos rodar o projeto em Local Host para simular. Nesse contexto já conseguimos visualizar o conversationID onde cada chamado atralada a um ID único(usuário por browser) e ver o fluxo
do chatbot já criado. As respostas vão sendo armazenados em variáveis e atrelhado ao conversationID. COnseguimos ver também as porcentagens de acerto na identificação de intenções(nível de acerto). Outro importante insight que podemos tirar é que a partir no nível de acerto das intenções podemos treinar o modelo, parte mais importante para ajustar o modelo
Uma das opçoes para trabalhar na estrutura de backend, conexão de API's é o Node JS.

Desafio interessante! Seguirei implementando o modelo! 



