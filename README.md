# Chatbot-Watson

Segue no link abaixo prévia do Chatbot Watson desenvolvido para clientes que querem montar um cardápio com opções de protéina, e ainda escolher o ponto da carne vermelha. No cardápio é possível escolher opções de legumes e arroz(normal ou integral) e concomitantemente tirar dúvidas sobre os alimentos.
Ao finalizar o pedido o assistente virtual confirma novamente o pedido e simula a transação financeira, pedindo ao usuário para inserir email. Inserido o email o assistente confirmar envio do email e passa número de telefone do restaurante FIT & Meals em caso de dúvida.

#https://assistant-chat-us-south.watsonplatform.net/web/public/f35cac3b-aeff-4eb4-a0e5-e75ded92ddda

O presente projeto é apenas uma prévia do assistente virtual. Sobre a construção do fluxo foi baseado em desambiguação e num conceito de fluxo fechado, onde o usuário tem no máximo 2 opções de rota para evitar que o assistente dê um resposta errada ou perca o sentido, ou até mesmo num cenário real o cliente não opte pela compra. Foram feito slotes para cada tipo de comida, em formato sequêncial simulando um formato de Menu para o usuário. A seleção é feita unidirecional e é requirido que o usuário digite algo para seguir.
No sequência de dúvida sobre os alimentos o fluxo seguiu com mesmo formato, porém com opção do usuário sair do Loop digitando não até sanar todas dúvidas. No final o usuário pode continuar questionando dúvida sobre os alimentos ou montar seu pedido, caindo no fluxo de montar cardápio.
