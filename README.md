# Booking
Challenge 2 - Check In/Booking application 

### **Sistema de Reserva de Hotel**
_Visão Geral_

Este projeto tem como objetivo criar uma aplicação utilizando Mulesoft para gerenciar reservas de hotéis. A aplicação receberá detalhes de reserva de vários hotéis, armazenará essas informações em um banco de dados e, três dias antes da data de check-in do hóspede, enviará um e-mail oferecendo a opção de realizar o check-in.

Para simplificar o desenvolvimento do projeto, foram constituídos três fluxos. Caso o projeto evolua, APIs separadas devem ser criadas para cada fluxo. Os três fluxos são os seguintes:

- Criar/Inserir Reserva no Banco de Dados

> Responsável por receber os detalhes da reserva e armazená-los no banco de dados.

- Enviar E-mail

> Agendado para ser executado três dias antes da data de check-in do hóspede, enviando um e-mail oferecendo a possibilidade de check-in.

- Atualizar Reserva

> Responsável por atualizar as informações da reserva conforme necessário.

### **Uso**

- O flow "createBooking" deve ser acionado sempre que uma nova reserva de hotel for feita.

- O flow "sendEmail" está agendado para ser executado através de um Scheduler que executará a cada 5 minutos, fazendo um SELECT na base de dados e selecionando Bookings com 3 posteriores a data atual e enviará um e-mail ao hóspede oferecendo a opção de realizar o check-in.

- O flow "updateBooking" será acionado através do Flow Reference implantado no flow "sendEmail" para atualizar as informações da reserva quando necessário.

### **Notas**

- Certifique-se de que as dependências necessárias estejam instaladas e configuradas no seu projeto Mule.

> Database Module

> 

Para desenvolvimento adicional ou aprimoramento, considere criar APIs separadas para cada fluxo a fim de manter a modularidade.

Sinta-se à vontade para contribuir, relatar problemas ou fornecer feedback!
